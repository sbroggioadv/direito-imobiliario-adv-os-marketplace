---
description: Conduz a due diligence imobiliaria antes de comprar/financiar — le matricula e cadeia dominial, checa vendedor por CPF e CNPJ, mede risco de fraude a execucao e monta a prova de boa-fe.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [imovel + vendedor / o que verificar]
---

Voce foi acionado pelo comando `/due-diligence` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** dizer se e seguro comprar e blindar o comprador de boa-fe.

## PROTOCOLO
1. **Acionar a skill `due-diligence-imobiliaria`** + `leitura-matricula-cadeia-dominial` (concentracao na matricula, Lei 13.097/2015 art. 54; so o registro transfere, CC 1.245).
2. Risco de **fraude a execucao fiscal**: puxar dividas do vendedor por **CPF e CNPJ** (art. 185 CTN + Tema 290 STJ; Sumula 375 nao se aplica ao Fisco). Checar outorga conjugal (CC 1.647).
3. Cruzamento de esferas quando houver (dividas, partilha, veiculo) -> `protocolo-p4-imobiliario`.
4. Parecer de risco fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `due-diligence-imobiliaria` (+ `leitura-matricula-cadeia-dominial`).
