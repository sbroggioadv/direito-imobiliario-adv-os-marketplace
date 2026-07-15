# direito-imobiliario-adv-os — regras internas do plugin

> Sistema operacional do advogado imobiliário brasileiro. Extrajudicial/registral/cartorário + judicial ponta-a-ponta. Despersonalizado (autoria IA Combativa; o escritório do cliente é configurado via `/start-imobiliario`).

## Invioláveis (anti-alucinação por design)
- **Nenhuma citação** de dispositivo/súmula/tema/alíquota entra em peça sem estar ancorada no `context/`. O guard é a skill `anti-alucinacao-imobiliaria`; a validação final é `suprema-corte-imobiliaria` (R1-R4) + `validador-imobiliario`.
- **Lei VIGENTE 2026 manda.** Nunca citar redação revogada. Atenção às reformas capturadas: Marco Legal das Garantias (Lei 14.711/2023), SERP (Lei 14.382/2022), Lei do Distrato (13.786/2018), Taxa Legal (Lei 14.905/2024), LC 214/2025 e LC 227/2026.
- **Postura honesta:** avisar rachas vivos (Súmula 308 × alienação fiduciária; Tema 796 holding; retenção 50% distrato; LC 227 × Tema 1.113 ITBI). Nunca prometer vitória onde há divergência.
- **Standalone-first:** funciona sozinho no Claude App/Cowork; cross-link com outros plugins é SOFT (ponteiro), nunca dependência.

## Fatos-âncora (os que blindam o produto — todos ✅ verificados em fonte oficial)
- Transmissão só com registro (CC 1.245); concentração na matrícula (Lei 13.097/2015 art. 54).
- ITBI: base = valor de mercado declarado (Tema 1.113 STJ / REsp 1.937.821); imunidade só até o capital integralizado (Tema 796 STF); tensão com a LC 227/2026.
- Usucapião extrajudicial 216-A (silêncio do confinante = concordância **desde a Lei 13.465/2017**); adjudicação compulsória extrajudicial 216-B (Lei 14.382/2022, independe de registro prévio).
- Alienação fiduciária 9.514 + Marco 14.711/2023 (leilão 60d, 2º leilão metade da avaliação, AF sucessiva, 26-A residencial exonera saldo); hipoteca agora tem execução extrajudicial.
- Locação 8.245: 4 garantias (art. 37); purga da mora 15d da citação, vedada em 24 meses; fiador penhorável resid. E comercial (Tema 1.127 STF); renovatória decadência 1 ano-6 meses.

## Fronteiras (cross-link soft, NÃO duplicar)
`civel` (processual) · `execucao` (execução) · `tributario-societario`/`holding` (ITCMD, planejamento, holding) · `familia` (partilha) · `bancario` (veículo DL 911) · `calculosjudiciais` (distrato/aluguéis/SELIC-IPCA).
