---
description: Escolhe e redige a acao real/possessoria correta — possessorias (reintegracao/manutencao/interdito), reivindicatoria e imissao na posse, usucapiao judicial, adjudicacao judicial, nunciacao/demolitoria e demarcatoria/divisoria — com a moldura processual certa.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [o que o autor quer / descricao do caso]
---

Voce foi acionado pelo comando `/acao` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** identificar a acao imobiliaria adequada e redigir a peca certa.

## PROTOCOLO
1. Classificar o objetivo material -> selecionar a skill:
   - Proteger **posse** (esbulho/turbacao/ameaca) -> **`acoes-possessorias`** (fungibilidade CPC 554; **forca nova x velha** CPC 558 define a liminar do 562).
   - Reaver a coisa como **proprietario** / imitir na posse -> **`reivindicatoria-e-imissao-na-posse`** (CC 1.228).
   - Propriedade pela posse com litigio -> **`usucapiao-judicial`**.
   - Escritura do vendedor renitente com litigio -> **`adjudicacao-compulsoria-judicial`** (CPC 501).
   - Obra/predio vizinho (obra nova, ruina, dano infecto CC 1.277/1.280) -> **`nunciacao-demolitoria`**.
   - Estremar limites/quinhoes -> **`demarcatoria-divisoria-e-embargos-terceiro`** (CPC 569-598; embargos de terceiro do promissario **Sumula 84 STJ**).
   - Comecar a peca do zero -> **`peticao-inicial-imobiliaria`**.
2. SEMPRE a moldura processual pela `base-processual-imobiliaria` (foro da situacao da coisa CPC 47 — competencia absoluta na possessoria/real; valor da causa CPC 292; rito).
3. Peca fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** a acao correspondente. Em duvida, deixe `imobiliario-master` dirimir.
