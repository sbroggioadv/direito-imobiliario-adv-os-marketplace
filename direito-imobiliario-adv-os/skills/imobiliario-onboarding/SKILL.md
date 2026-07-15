---
name: imobiliario-onboarding
description: Configura o escritório do advogado no plugin de Direito Imobiliário — coleta perfil, persona de atuação e preferências de peça, uma vez só. Use quando o advogado digitar /start-imobiliario, "configurar o escritório", "começar do zero", "me cadastra", na primeira vez que abrir o plugin, ou quando outra skill detectar que o escritório ainda não foi configurado. Faz as escolhas de lista fechada com botões (AskUserQuestion), nunca com menu de texto, e grava tudo para as demais skills reaproveitarem.
---

# imobiliario-onboarding — configuração do escritório

Roda **uma vez** (ou quando o advogado pedir para reconfigurar). Coleta o mínimo para personalizar peças e roteamento, sem burocracia. Persiste o resultado onde `memoria-de-caso-imobiliario` lê o perfil.

## Regra de interação
Toda escolha de lista fechada usa **AskUserQuestion** (botões clicáveis), uma pergunta por vez, com uma opção recomendada destacada. Campos abertos (nome, OAB, cidade) o advogado digita. **Nunca** desenhar menu numerado em texto.

## Bloco 1 — Identidade do escritório (campos abertos)
Pergunte e grave:
- Nome do advogado / banca (como assina as peças).
- OAB (seccional + número).
- Cidade/UF de atuação principal (define foro-padrão e cartório de referência).
- Comarca/foro habitual (opcional).

> Isso alimenta o cabeçalho/assinatura das peças. **Não** use nenhum nome real de exemplo — o valor vem do advogado.

## Bloco 2 — Persona de atuação (AskUserQuestion)
Pergunta: **"Como você atua no imobiliário?"** — opções (multi-seleção permitida):
- **Advogado avulso / banca** — atende clientes variados, contencioso + consultivo. *(recomendado padrão)*
- **Jurídico de imobiliária / incorporadora** — foco em contratos, distrato, incorporação, cobrança, locação em volume.
- **Cartorário / registral** — foco em usucapião e adjudicação extrajudicial, retificação, dúvida, REURB, pareceres registrais.

A persona ajusta o tom e o que a triagem oferece primeiro (ex.: cartorário → destaca a via extrajudicial; imobiliária → destaca contrato/distrato/locação).

## Bloco 3 — Lado predominante (AskUserQuestion)
Pergunta: **"Você costuma defender qual lado?"**
- **Comprador / adquirente / possuidor / locatário / condômino devedor**
- **Vendedor / incorporador / credor fiduciário / locador / condomínio**
- **Os dois, depende do caso** *(recomendado)*

Grava como preferência side-aware (a peça se adapta, mas cada caso confirma o lado real).

## Bloco 4 — Preferências de peça (AskUserQuestion)
- **Estilo de redação:** Objetivo e enxuto *(recomendado)* · Detalhado e doutrinário.
- **Citar jurisprudência sempre que houver âncora?** Sim *(recomendado)* · Só quando eu pedir.
- **Postura nos rachas:** Sempre avisar a divergência *(recomendado — padrão do plugin, não desligável de fato)*.

> Independentemente da resposta, o guard `anti-alucinacao-imobiliaria` e a `suprema-corte-imobiliaria` continuam obrigatórios: nenhuma citação sai sem âncora, e todo racha vivo é sinalizado.

## Fechamento
1. Resuma o perfil coletado em 4-5 linhas e confirme com o advogado.
2. Grave o perfil (via `memoria-de-caso-imobiliario`) para reuso automático.
3. Encaminhe: *"Escritório configurado. Rode `/imobiliario-master` para abrir um caso ou `/triagem` se quiser que eu identifique a trilha conversando."*

## Nunca
- Não invente dados do escritório nem preencha exemplos com nomes reais.
- Não repita o onboarding a cada sessão — só se o perfil não existir ou o advogado pedir.
