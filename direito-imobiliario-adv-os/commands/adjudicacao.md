---
description: Obtem a escritura do vendedor renitente por adjudicacao compulsoria — extrajudicial no cartorio (art. 216-B LRP, Lei 14.382/2022, independe de registro previo — Sumula 239 STJ) ou judicial (CPC 501).
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [promessa quitada + vendedor que recusa/sumiu]
---

Voce foi acionado pelo comando `/adjudicacao` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** transformar a promessa quitada em propriedade quando o vendedor nao outorga a escritura.

## PROTOCOLO
1. **Extrajudicial primeiro:** promessa quitada e vendedor recusa/sumiu -> **`adjudicacao-compulsoria-extrajudicial`** (art. 216-B LRP; **independe de registro previo** da promessa — Sumula 239 STJ). Mais rapida e barata; nenhum plugin irmao cobre.
2. Se houver litigio real (vicio, disputa de dominio) -> **`adjudicacao-compulsoria-judicial`** — a **sentenca supre a declaracao de vontade** e produz os efeitos da escritura nao emitida (**CPC 501**, apos transito).
3. Base processual pela `base-processual-imobiliaria` (foro da situacao da coisa, CPC 47).
4. Peca/requerimento fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `adjudicacao-compulsoria-extrajudicial` OU `adjudicacao-compulsoria-judicial` conforme o caso.
