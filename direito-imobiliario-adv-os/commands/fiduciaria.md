---
description: Atua na alienacao fiduciaria de imovel e na hipoteca — consolidacao, leilao e purga da mora (Lei 9.514 + Marco das Garantias 14.711/2023) ou defesa do devedor, e execucao extrajudicial da hipoteca no RI.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [financiamento/garantia + fase (consolidacao/leilao/defesa)]
---

Voce foi acionado pelo comando `/fiduciaria` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** conduzir garantia real de imovel (credor ou devedor), extrajudicial primeiro.

## PROTOCOLO
1. **Alienacao fiduciaria:** **`alienacao-fiduciaria-imovel`** — Lei 9.514/97 + **Marco 14.711/2023** (leilao em 60 dias, 2 leilao pela metade da avaliacao, AF sucessiva, art. 26-A exonera saldo em imovel residencial). Segue a Lei 9.514, **nao o CDC** (Tema 1.095 STJ). Purga da mora garantida.
2. **Racha vivo:** Sumula 308 (hipoteca do incorporador nao opoe ao adquirente) x AF -> a 4 Turma nega a extensao. **Avisar** (postura honesta).
3. **Hipoteca:** **`hipoteca-e-execucao-extrajudicial`** — o Marco das Garantias abriu a **execucao extrajudicial no RI** (contrato tambem e titulo executivo, CPC 784 V).
4. Peca/defesa fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `alienacao-fiduciaria-imovel` e/ou `hipoteca-e-execucao-extrajudicial`.
