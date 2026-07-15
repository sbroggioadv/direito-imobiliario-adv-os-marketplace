---
description: Resolve demandas de condominio e associacao — instituicao/convencao, cobranca de cotas (titulo executivo extrajudicial, CPC 784 X, obrigacao propter rem), assembleia/governanca, condomino antissocial e multipropriedade.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [tipo de demanda condominial]
---

Voce foi acionado pelo comando `/condominio` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** atacar a demanda condominial pela skill certa.

## PROTOCOLO
1. Classificar e rotear:
   - Instituir/convencionar -> **`instituicao-e-convencao-condominio`**.
   - Cobrar cota -> **`cobranca-cotas-condominiais`** (**cota e titulo executivo extrajudicial** — CPC 784 X; obrigacao *propter rem*, CC 1.345 — executa direto).
   - Assembleia, quorum, prestacao de contas, sindico -> **`assembleia-e-governanca-condominial`**.
   - Condomino antissocial (CC 1.337) ou multipropriedade (Lei 13.777/2018) -> **`condominio-de-lotes-e-multipropriedade`**.
   - Associacao de moradores / loteamento fechado -> **`constituicao-associacoes`**.
2. Base processual pela `base-processual-imobiliaria` (foro; execucao vs conhecimento).
3. Peca fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** a skill condominial correspondente. Em duvida, deixe `imobiliario-master` dirimir.
