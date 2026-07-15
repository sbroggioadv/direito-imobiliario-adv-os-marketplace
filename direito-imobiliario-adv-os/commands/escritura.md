---
description: Prepara a escritura publica / instrumento de transmissao e a minuta de registro — requisitos, outorga conjugal, tributos (ITBI) e concentracao na matricula ate o registro que transfere a propriedade.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [tipo de ato + partes + imovel]
---

Voce foi acionado pelo comando `/escritura` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** montar a escritura/instrumento e levar o titulo ao registro.

## PROTOCOLO
1. **Acionar a skill `escritura-e-instrumento`** — qualificacao, descricao do imovel pela matricula, **outorga conjugal** (CC 1.647; ausencia = anulavel, CC 1.649), quitacao/preco, tributos.
2. Lembrar: **so o registro transfere** (CC 1.245); a escritura e titulo, o dominio nasce no RI. ITBI recolhido antes do registro -> cross-link `itbi`.
3. Instrumento particular com forca de escritura em hipoteses legais (ex.: SFH) quando cabivel.
4. Ato/minuta fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `escritura-e-instrumento`.
