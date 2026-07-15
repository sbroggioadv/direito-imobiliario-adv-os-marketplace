---
description: Conduz demandas de locacao (Lei 8.245) — contrato e garantias (art. 37), despejo, renovatoria (decadencia 1 ano a 6 meses), revisional (apos 3 anos), execucao de alugueis/encargos (CPC 784 VIII) e defesa do fiador.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [tipo de demanda locaticia]
---

Voce foi acionado pelo comando `/locacao` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** atacar a demanda de locacao pela skill e prazo corretos.

## PROTOCOLO
1. Classificar e rotear:
   - Redigir contrato / escolher garantia (art. 37: caucao, fianca, seguro-fianca, cessao de quotas) -> **`contrato-locacao`**.
   - Despejo (falta de pagamento com **purga da mora em 15 dias da citacao**, vedada se usada nos 24 meses; denuncia vazia; infracao) -> **`acao-despejo`**.
   - Renovatoria -> **`acao-renovatoria`** (⚠️ **decadencia: 1 ano a 6 meses** do fim do prazo — fatal).
   - Revisional -> **`revisional-de-aluguel`** (cabivel **apos 3 anos**).
   - Executar alugueis/encargos -> **`execucao-alugueis-e-encargos`** (**titulo executivo extrajudicial** — CPC 784 VIII).
   - Defender inquilino/fiador -> **`locacao-defesa-e-fiador`** (fiador penhoravel resid. **e** comercial — Tema 1.127 STF + Sumula 549 STJ).
2. Base processual pela `base-processual-imobiliaria`.
3. Peca fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** a skill de locacao correspondente. Em duvida, deixe `imobiliario-master` dirimir.
