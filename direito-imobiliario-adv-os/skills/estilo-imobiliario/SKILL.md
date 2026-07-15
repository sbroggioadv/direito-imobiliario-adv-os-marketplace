---
name: estilo-imobiliario
description: Voz, estrutura e formatação padrão das peças e pareceres do plugin imobiliário — como qualificar o imóvel, endereçar ao foro certo, fixar valor da causa, citar dispositivo vigente e escrever com clareza técnica. Use quando o advogado for redigir qualquer peça/parecer imobiliário e quiser padronizar o texto, quando outra skill produzir a peça (é a camada de acabamento), ou ao formatar endereçamento, qualificação, descrição do imóvel, pedidos e citações.
---

# Estilo imobiliário — a voz das peças

Camada de acabamento: garante que toda peça/parecer do plugin saia com a **mesma voz técnica**, o imóvel **descrito certo** e o **dispositivo vigente**. É invocada pelas skills de peça antes do fechamento pela Suprema Corte.

## 1. Voz
- **Engenheiro-advogado sênior:** direto, técnico, sem retórica vazia. Frase curta. Um argumento por parágrafo.
- **Afirmação ancorada:** cada tese vem com o dispositivo/tema/súmula. Sem "é pacífico que" solto.
- **Postura honesta:** onde há racha, o texto **diz** (não esconde para parecer mais forte). Isso é diferencial, não fraqueza.
- **Despersonalizado:** nunca inserir nome de escritório, OAB ou advogado no corpo — esses dados vêm do onboarding do cliente (`/start-imobiliario`). Autoria institucional.

## 2. Anatomia da peça (ajuste ao tipo)
1. **Endereçamento** — juízo **do foro da situação do imóvel** (competência das ações reais/possessórias/locatícias); administrativa vai ao **Oficial do RI** ou ao **Juízo Corregedor**.
2. **Qualificação** das partes (+ estado civil/regime de bens — decisivo em outorga conjugal).
3. **Descrição do imóvel — idêntica à matrícula:** número da **matrícula**, **Registro de Imóveis** e comarca, área, confrontações. Divergência entre peça e matrícula é causa de inépcia/indeferimento. Sempre juntar **certidão atualizada (≤ 30 dias)**.
4. **Dos fatos** — narrativa limpa, cronológica, ancorada em documento.
5. **Do direito** — por tópico, com dispositivo vigente.
6. **Dos pedidos** — específicos, exequíveis, na ordem lógica (tutela → mérito → sucumbência).
7. **Valor da causa** — locação = **12 meses de aluguel** (art. 58, II, Lei 8.245 ✅); real = valor do imóvel/proveito; revisional = 12× a diferença pretendida.
8. **Provas e requerimentos** finais; fecho.

## 3. Como citar (padrão do plugin)
- **Lei:** "art. X da Lei Y" / "art. X do CC". Confirmar redação **vigente** — muitas mudaram (ver §4).
- **Súmula:** "Súmula NN do STJ/STF" + enunciado quando load-bearing.
- **Tema repetitivo/RG:** "Tema NNN do STJ/STF (REsp/RE ...)". **ITBI é REsp 1.937.821, não RE** ✅.
- Nunca citar número "de memória" — só o que está ancorado em `context/`; o `validador-imobiliario` confere antes do selo.

## 4. Checklist anti-desatualização (colar mentalmente antes de assinar)
- **Arras:** art. 418 do CC = **nova redação da Lei 14.905/2024** (incisos I/II + honorários) — não a antiga ✅.
- **Juros/correção legais:** **SELIC deduzido do IPCA** (Lei 14.905/2024) — **não** "1% ao mês" ✅.
- **Usucapião extrajudicial:** silêncio do confinante = **concordância desde a Lei 13.465/2017** — não "novidade 2026", não "silêncio = discordância" ✅.
- **Hipoteca:** tem **execução extrajudicial** (Lei 14.711/2023) — não "só judicial" ✅.
- **AF:** cabe **2ª AF sucessiva/superveniente** (art. 22, §§3-4, Lei 9.514 ✅); leilão **60 dias**, 2º leilão aceita **metade da avaliação**; **26-A** residencial exonera saldo ✅.
- **ITBI:** base = valor de mercado **declarado** (Tema 1.113) — não valor venal de IPTU nem "valor de referência"; **tensão com a LC 227/2026** ✅.
- **Locação:** **4 garantias** (art. 37 — a 4ª é cessão fiduciária de quotas); purga **15 dias da citação**, vedada se usada nos **24 meses**; renovatória decai em **1 ano a 6 meses** (fatal); fiador penhorável resid. **E** comercial (Tema 1.127) ✅.
- **Distrato:** 25% comum / 50% afetação (Lei 13.786), com mitigação 50%→25% por CC 413; contrato pré-2018 segue Súmula 543 — **delimitar pela data do contrato** ✅.
- **Adjudicação extrajudicial** (216-B): independe de registro prévio da promessa (§2º) ✅.
- **IBS/CBS na locação** (LC 214/2025): "aluguel só paga IR" está morto ✅.

## 5. Itens que NÃO se afirmam como fato (só "a confirmar")
Lei 14.825/2024, Súmula 194 "contemporânea", prazo de 15d do art. 216-B, alíquota reduzida do RET, RMS 27.358, REsp 2.175.618 (racha distrato). Podem ser mencionados como pendentes de verificação — nunca como âncora fechada.

## 6. Fechamento
O estilo **não substitui** a revisão de conteúdo: toda peça segue para **`suprema-corte-imobiliaria`** (R1-R4) + **`validador-imobiliario`**. Guard `anti-alucinacao-imobiliaria` sempre ligado.
