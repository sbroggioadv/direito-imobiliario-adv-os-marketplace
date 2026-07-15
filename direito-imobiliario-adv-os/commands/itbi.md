---
description: Trata o ITBI da transmissao — base de calculo (valor de mercado declarado, Tema 1.113 STJ), imunidade na integralizacao de holding (Tema 796 STF, so ate o capital) e defesa contra arbitramento a maior, com a tensao da LC 227/2026.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [operacao + municipio + valor / cobranca]
---

Voce foi acionado pelo comando `/itbi` do plugin direito-imobiliario-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** apurar/defender o ITBI correto da operacao.

## PROTOCOLO
1. **Acionar a skill `itbi-transmissao`** — base = **valor de mercado declarado** pelo contribuinte (**Tema 1.113 STJ / REsp 1.937.821**), nao o "valor de referencia" arbitrado de oficio pelo municipio.
2. **Imunidade na integralizacao** de capital com imoveis: so ate o **capital integralizado** (**Tema 796 STF**); atividade imobiliaria preponderante afasta. Ha **tensao com a LC 227/2026** -> postura honesta.
3. Cross-link soft `tributario-societario`/`holding` para o planejamento; aqui e o tributo do imovel.
4. Defesa/consulta fecha pela `suprema-corte-imobiliaria` + `validador-imobiliario`.

**Skill a acionar:** `itbi-transmissao`.
