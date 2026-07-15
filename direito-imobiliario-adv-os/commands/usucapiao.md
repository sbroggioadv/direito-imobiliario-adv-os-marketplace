---
description: Conduz a usucapiao pela via certa — extrajudicial no cartorio (art. 216-A LRP, silencio do confinante = concordancia desde a Lei 13.465/2017) ou judicial, escolhendo a modalidade e o prazo aplicavel.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [posse + tempo + modalidade / imovel]
---

Voce foi acionado pelo comando `/usucapiao` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** regularizar a propriedade pela posse, preferindo o cartorio.

## PROTOCOLO
1. **Extrajudicial primeiro:** posse mansa com requisitos + ata notarial -> **`usucapiao-extrajudicial`** (art. 216-A LRP; **silencio do confinante = concordancia desde a Lei 13.465/2017**). E o diferencial do plugin.
2. Se houver litigio/oposicao ou faltar requisito para o cartorio -> **`usucapiao-judicial`** (base processual `base-processual-imobiliaria`; citacao pessoal dos confinantes, CPC 246 §3 — dispensada em unidade autonoma de condominio).
3. Definir a **modalidade** (extraordinaria, ordinaria, especial urbana/rural, familiar) e o **prazo** conforme a posse. Bem publico nao usucape (Sumula 340 STF / CF 183 §3).
4. Peca/requerimento fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `usucapiao-extrajudicial` OU `usucapiao-judicial` conforme o caso.
