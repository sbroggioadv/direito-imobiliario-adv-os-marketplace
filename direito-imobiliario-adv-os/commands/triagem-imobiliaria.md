---
description: Classifica a demanda imobiliaria (uma das 12 trilhas) e indica a skill, a via (extrajudicial/judicial/administrativa) e os alertas de prazo/racha corretos.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [descricao do caso]
---

Voce foi acionado pelo comando `/triagem-imobiliaria` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** classificar e rotear o caso, separando o que o cartorio resolve do que precisa de acao.

## PROTOCOLO
1. **Acionar a skill `triagem-imobiliaria`** (by-conversation, botoes via AskUserQuestion) — identifica a trilha (1 das 12) + skill(s)-alvo + via recomendada + alertas de prazo/racha.
2. **Extrajudicial antes de judicial:** sempre que couber cartorio, oferecer a via extrajudicial primeiro.
3. Se tocar mais de uma esfera, sinalizar `protocolo-p4-imobiliario` + cross-link soft.
4. Encaminhar ao `imobiliario-master` e registrar em `memoria-de-caso-imobiliario`.

**Skill a acionar:** `triagem-imobiliaria`.
