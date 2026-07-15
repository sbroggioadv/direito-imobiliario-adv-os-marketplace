---
name: validador-imobiliario
description: "Gate anti-alucinacao do plugin: valida vigencia e existencia de dispositivo, sumula, tese, tema, aliquota e prazo ANTES de qualquer citacao entrar em peca. Cruza com context/ (CC direitos reais, LRP/SERP, Lei 9.514/Marco 14.711, Lei 8.245, condominio/incorporacao, loteamento/REURB, ITBI/reformas, jurisprudencia) e, na duvida, exige checagem ao vivo (fetch real) ou bloqueia. Integra o guard global anti-alucinacao-juridica. Use antes de citar qualquer fundamento, ou quando o operador disser valida essa jurisprudencia, esse artigo existe, essa sumula esta vigente, esse tema/acordao existe, confere essa aliquota, esse dispositivo ainda vige, checa esse prazo."
---

# VALIDADOR-IMOBILIARIO — Gate anti-alucinacao (dispositivos + jurisprudencia + numeros)

> Camada 1 (Fundacao). Trava de seguranca. Nenhuma citacao — legal, jurisprudencial, aliquota ou prazo — entra em peca sem passar por aqui. Distinto da `suprema-corte-imobiliaria` (gate final da peca inteira): este valida cada CITACAO.

## Anexos obrigatorios (context/) — grep do item, ler a faixa
- `context/cc-direitos-reais.md` — CC (direitos reais + contratos: arras 418, juros/correcao 389/406).
- `context/lrp-6015-serp.md` — LRP 6.015/73 + SERP 14.382/22 (216-A, 216-B, 213, 198-204) + Lei 13.097/15 art. 54.
- `context/lei-9514-marco-garantias.md` — AF + Marco 14.711/2023 (arts. 22-27-A, 26-A).
- `context/lei-8245-locacao.md` — locacao (despejo 59/62, renovatoria 51/52, revisional 19, garantias 37).
- `context/condominio-incorporacao.md` — CC 1.331-1.358 + Lei 4.591 + Lei 13.786.
- `context/loteamento-reurb.md` — Lei 6.766 + Lei 13.465.
- `context/itbi-e-reformas-tributarias.md` — Tema 1.113 + 796 + LC 227/2026 + LC 214/2025 + Lei 14.905/2024.
- `context/jurisprudencia-imobiliaria.md` — corpus com selos ✅/🟡/🔴.

## Objetivo
Impedir que qualquer dispositivo, sumula, tese, tema, aliquota ou prazo **inexistente, revogado, alterado ou nao verificado** entre numa peca. Veredito binario por citacao: **VALIDADO** ou **BLOQUEADO**.

## Quando ativar
- Antes de inserir qualquer citacao numa peca/parecer/recurso.
- O operador pede para conferir artigo, sumula, tema, aliquota, prazo ou ementa.
- Outra skill propos um fundamento e precisa do sinal verde.

## Metodologia
1. **Dispositivo de lei:** grep do artigo no anexo certo e ler a faixa — o numero/redacao **existe e esta vigente?** Confirmar a **redacao pos-reforma** onde houver (arras **418 = Lei 14.905/2024**; AF **22-27-A/26-A = Lei 14.711/2023**; 216-A/216-B/198 = **Lei 14.382/2022**).
2. **Jurisprudencia:** achar no corpus `jurisprudencia-imobiliaria.md`. **✅** → VALIDADO; **🟡** → so VALIDADO apos conferir inteiro teor **ao vivo**; **🔴/nao consta** → busca ao vivo obrigatoria (WebSearch/WebFetch na fonte oficial STJ/STF; Firecrawl/Perplexity fallback). So VALIDADO se a pagina **abrir** e o teor **constar**, com link.
3. **Aliquota/prazo:** conferir contra o anexo tributario/registral. Aliquota inventada ou prazo nao ancorado = BLOQUEADO.
4. **Veredito por citacao:** VALIDADO (com fonte) ou BLOQUEADO (motivo). Na duvida → **BLOQUEADO**.
5. Acionar o guard global `anti-alucinacao-juridica` em paralelo.

## Correcoes TRAVADAS (bloquear se aparecerem errados)
- **Tema 1.095 ≠ purgacao** (e "AF afasta CDC"); purgacao = **Tema 1.288 PENDENTE** + REsp 1.649.595 (racha temporal).
- **Sumula 619 = bem publico** (mera detencao), nao usucapiao urbano.
- **Sumula 486 = imovel locado bem de familia**, nao cota condominial (penhora por cota = **Lei 8.009 art. 3º IV**).
- **"REsp" 1.937.821** (Tema 1.113), nao "RE".
- **Arras art. 418** = redacao **Lei 14.905/2024**; **juros/correcao = SELIC-IPCA** (14.905/2024), nao "1% a.m.".
- **Hipoteca** tem **execucao extrajudicial** (Lei 14.711/2023) — bloquear "so judicial".
- **Base do ITBI** = valor declarado (**Tema 1.113**), nao valor venal do IPTU nem "valor de referencia".
- **Silencio do confinante na usucapiao extrajud. (216-A §2º) = CONCORDANCIA** (desde **Lei 13.465/2017**), nao discordancia.
- **REsp 2.173.311/PE** (due diligence): usar como **ALERTA** ancorado em **art. 185 CTN + Tema 290 STJ** (fraude a exec. fiscal; presuncao absoluta pos-divida ativa; Sumula 375 nao se aplica). Puxar PGFN por **CPF e CNPJ** do vendedor empresario individual. **Nao dizer "tese/presuncao nova".**
- **Locacao = 4 garantias (Lei 8.245 art. 37)**; purga do despejo **15 dias da citacao**, vedada se usada nos **24 meses**; **fiador comercial penhoravel (Tema 1.127)**; renovatoria decadencia **1 ano a 6 meses** (fatal).

## 🟡 PROIBIDO afirmar sem verificacao (bloquear como fato)
Lei 14.825/2024 · Sumula 194 "contemporanea" · **prazo de 15d do art. 216-B** · aliquota reduzida do RET · RMS 27.358 · REsp 2.175.618. Podem constar como "a confirmar", nunca como fato.

## Entrega obrigatoria final
Lista de citacoes com veredito (VALIDADO/BLOQUEADO) + fonte/ponteiro + motivo. Versao corrigida das que passam; as bloqueadas saem da peca. Havendo reforma incidente, apontar a redacao vigente correta.

## Guard
Default no incerto e **BLOQUEAR**. Nada inventado, nada revogado, nada 🟡 sem conferencia. Sem fonte real aberta, nao valida. Trabalha com `jurisprudencia-imobiliaria` + guard global `anti-alucinacao-juridica`; entrega para a `suprema-corte-imobiliaria`.
