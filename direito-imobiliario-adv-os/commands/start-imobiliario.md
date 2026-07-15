---
description: Inicia o wizard de configuracao do plugin de Direito Imobiliario — cria a pasta imobiliario/ com identidade do escritorio, areas de atuacao, cartorios/tribunais-alvo, polo preferencial e modo de fluxo.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [--update para reconfigurar]
---

Voce foi acionado pelo comando `/start-imobiliario` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** configurar o plugin de Direito Imobiliario ao perfil do escritorio.

## PROTOCOLO
1. **Acionar a skill `imobiliario-onboarding`** (wizard com botoes via AskUserQuestion nas escolhas de lista fechada).
2. Cria `<cwd>/imobiliario/perfil.md` (identidade, areas, comarcas/cartorios-alvo, polo preferencial, modo).
3. Se ja existir, oferecer continuar / atualizar / recriar.

**Skill a acionar:** `imobiliario-onboarding`.
