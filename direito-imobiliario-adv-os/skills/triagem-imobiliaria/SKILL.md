---
name: triagem-imobiliaria
description: Identifica, conversando, qual das 12 trilhas do Direito Imobiliário o caso do advogado percorre e devolve a rota para a skill certa. Use quando o advogado digitar /triagem, chegar com um caso confuso ou misto ("tenho um problema com um imóvel", "não sei se é possessória ou petitória", "comprei e o vendedor sumiu"), ou quando o imobiliario-master precisar classificar antes de rotear. Faz perguntas de lista fechada com botões (AskUserQuestion), separa via extrajudicial de judicial e aponta o cruzamento de esferas quando houver.
---

# triagem-imobiliaria — classificação by-conversation

Objetivo: em poucas perguntas, dizer **qual trilha** e **qual skill** atacam o caso — sem judicializar o que o cartório resolve. Use **AskUserQuestion** (botões) nas escolhas fechadas; texto livre só para o relato inicial. Ao terminar, devolva a trilha ao `imobiliario-master` e registre em `memoria-de-caso-imobiliario`.

## Passo 1 — Natureza da demanda (AskUserQuestion)
**"O que você precisa resolver?"**
- **Fazer/desfazer um negócio** (comprar, vender, permutar, incorporar, lotear, distratar)
- **Regularizar no cartório** (registrar, usucapir, adjudicar, retificar, REURB)
- **Brigar pela posse/propriedade** (esbulho, reintegração, usucapião judicial, imissão)
- **Condomínio** (cotas, convenção, assembleia)
- **Locação** (aluguel, despejo, renovatória, fiador)
- **Financiamento/garantia** (alienação fiduciária, hipoteca, leilão)
- **Tributo do imóvel** (ITBI, imunidade)
- **Recorrer / defender em processo em curso**

## Passo 2 — Perguntas de desempate por ramo
Faça só as que o relato exigir (AskUserQuestion):
- **Negócio:** já tem contrato assinado? registrado? quitado? quem deu causa ao desfazimento? contrato **antes ou depois de 2018**? (define distrato: Súmula 543 × Lei 13.786).
- **Regularizar:** tem promessa quitada e vendedor recusa/sumiu? → **adjudicação extrajudicial** (216-B, Súmula 239). Posse mansa com prazo? → **usucapião extrajudicial** (216-A). Erro na descrição? → **retificação** (213). Núcleo urbano informal? → **REURB**.
- **Posse:** o esbulho/turbação tem **menos ou mais de ano e dia**? (art. 558 CPC — força nova × velha, define liminar). Bem público envolvido? (não usucape — Súmula 340 STF/CF 183 §3º).
- **Condomínio:** é cobrança de cota (propter rem, CC 1.345) · vício de assembleia · condômino antissocial (1.337) · multipropriedade (13.777)?
- **Locação:** contrato residencial/comercial/built to suit? qual garantia (art. 37)? é despejo (fundamento?), renovatória (checar **prazo 1 ano-6 meses**), revisional (**após 3 anos**) ou defesa de fiador?
- **Garantia:** alienação fiduciária registrada? já houve consolidação/leilão? cabe **purga da mora** (15d)?
- **Tributo:** município arbitrou base por "valor de referência"? (Tema 1.113 — defesa). Integralização em holding? (Tema 796 — só até o capital).

## Passo 3 — Extrajudicial antes de judicial
Sempre que couber cartório (adjudicação/usucapião extrajudicial, retificação, hipoteca no RI), **ofereça a via extrajudicial primeiro** — mais rápida e barata. É o diferencial do plugin.

## Passo 4 — Cruzamento de esferas
Se o caso tocar mais de uma esfera (ex.: due diligence com dívida fiscal do vendedor; imóvel em partilha; veículo em DL 911), sinalize e sugira `protocolo-p4-imobiliario` + o cross-link soft (`tributario-societario`, `familia`, `bancario`, `execucao`, `calculosjudiciais`).

## Saída
Devolva: **(1)** trilha (1 das 12 do master), **(2)** skill(s)-alvo, **(3)** via recomendada (extrajudicial/judicial/administrativa), **(4)** alertas de prazo/racha detectados. Sem inventar dispositivo — o guard `anti-alucinacao-imobiliaria` vale aqui também.
