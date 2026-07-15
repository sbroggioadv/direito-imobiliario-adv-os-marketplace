---
description: Porta unica do plugin de Direito Imobiliario — descreva a demanda em linguagem natural e o orquestrador triangula a trilha, dirime todas as skills e conduz o caso ate a peca/parecer revisado.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [descricao da demanda imobiliaria]
---

Voce foi acionado pelo comando `/imobiliario-master` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** conduzir qualquer demanda de Direito Imobiliario de ponta a ponta (extrajudicial/registral + judicial).

## PROTOCOLO
1. **Acionar a skill `imobiliario-master`** — le `context/metodologia-imobiliaria.md`, classifica via `triagem-imobiliaria`, abre/atualiza `memoria-de-caso-imobiliario`. Guard `anti-alucinacao-imobiliaria` sempre ligado.
2. Roteia para uma das 12 trilhas (contrato, due diligence, registral, ITBI, REURB, condominio, locacao, acao real/possessoria, fiduciaria/hipoteca, defesa/incidente, recurso, consultivo).
3. **Extrajudicial primeiro** (o fosso do plugin): oferecer a via de cartorio (adjudicacao/usucapiao extrajudicial, retificacao, hipoteca no RI) antes de judicializar.
4. Toda peca/contrato/parecer fecha pela `suprema-corte-imobiliaria` (R1-R4) + `validador-imobiliario`.

**Skill a acionar:** `imobiliario-master`.
