---
description: Escolhe e redige o recurso imobiliario correto (ED, agravo de instrumento, apelacao, REsp/RE, agravo em recurso excepcional) ou as contrarrazoes/contraminuta, com admissibilidade e tempestividade.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [decisao a recorrer]
---

Voce foi acionado pelo comando `/recurso` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** recorrer da decisao correta, no recurso certo.

## PROTOCOLO
1. Identificar a decisao:
   - Vicio (omissao/contradicao/obscuridade/erro material) -> **`embargos-de-declaracao`** (CPC 1.022; **5 dias**, sem preparo).
   - Interlocutoria do rol CPC 1.015 (tutela, merito, etc.) -> **`agravo-de-instrumento`**.
   - Sentenca -> **`apelacao-imobiliaria`** (CPC 1.009-1.014; dirigida ao 1 grau, contrarraz. 15 dias).
   - Ultima instancia vs lei federal/CF -> **`recursos-excepcionais`** (REsp = CF 105 III / RE = CF 102 III; CPC 1.029).
   - Inadmissao de REsp/RE -> **`agravos-excepcionais`** (CPC 1.042).
   - Responder recurso da parte contraria -> **`contrarrazoes-e-contraminuta`**.
2. SEMPRE checar **admissibilidade e tempestividade** (cabimento, prazo em dias uteis, preparo) via `base-processual-imobiliaria`.
3. Peca fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** o recurso correspondente. Em duvida, deixe `imobiliario-master` dirimir.
