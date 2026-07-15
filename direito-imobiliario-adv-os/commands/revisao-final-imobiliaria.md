---
description: Gate de revisao final R1-R4 (Suprema Corte Imobiliaria) + validador antes de qualquer entrega — audita competencia/foro, fundamentacao vigente, jurisprudencia real e forma/prazos/valor da causa.
allowed-tools: Read, Grep, Glob
argument-hint: [peca/contrato/parecer a validar]
---

Voce foi acionado pelo comando `/revisao-final-imobiliaria` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** auditar a entrega antes de liberar. Sem selo, nao sai.

## PROTOCOLO
1. **Acionar a skill `suprema-corte-imobiliaria`** — R1 (fatos/competencia/foro da situacao da coisa), R2 (fundamentacao **vigente 2026**: Marco 14.711/2023, SERP 14.382/2022, Distrato 13.786/2018, Taxa Legal 14.905/2024, LC 214/2025, LC 227/2026 — nunca redacao revogada), R3 (**jurisprudencia real** ✅ com WebFetch na fonte), R4 (forma/pedidos/tempestividade/valor da causa).
2. Rodar o **`validador-imobiliario`** — nenhum dispositivo/sumula/tema/aliquota sem ancora em `context/`.
3. **Postura honesta:** avisar rachas vivos (Sumula 308 x AF; Tema 796 holding; retencao 50%->25% CC 413; LC 227 x Tema 1.113 ITBI).
4. Veredito: LIBERADO ou CORRIGIR.

**Skill a acionar:** `suprema-corte-imobiliaria` (+ `validador-imobiliario`).
