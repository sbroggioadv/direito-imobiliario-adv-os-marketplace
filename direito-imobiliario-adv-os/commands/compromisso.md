---
description: Redige o compromisso/promessa de compra e venda de imovel — clausulas, arras, condicoes, distrato e direito de arrependimento conforme a data do contrato (Sumula 543 x Lei 13.786/2018).
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [partes + imovel + condicoes do negocio]
---

Voce foi acionado pelo comando `/compromisso` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** produzir um compromisso de compra e venda seguro e registravel.

## PROTOCOLO
1. **Acionar a skill `compromisso-compra-venda`** (apoiada por `base-contratual-imobiliaria`) — objeto, preco, arras (CC 417-420), condicoes, irretratabilidade, registro no RI (efeito de direito real, CC 1.417-1.418).
2. **Distrato:** delimitar pela **data do contrato** — pre-2018 segue Sumula 543 STJ; a partir de 2018, Lei 13.786 (25% comum / 50% afetacao, STJ mitiga 50%->25% por CC 413). Cross-link `distrato-imobiliario`.
3. Se o negocio ja estiver quitado e o vendedor se recusar/sumir -> apontar `adjudicacao` (extrajudicial primeiro, art. 216-B).
4. Contrato fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `compromisso-compra-venda`.
