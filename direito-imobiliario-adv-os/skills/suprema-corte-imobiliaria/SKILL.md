---
name: suprema-corte-imobiliaria
description: Auditoria de excelência R1-R4 que revisa toda peça, contrato ou parecer imobiliário antes da entrega — fatos/imóvel/matrícula, fundamentação vigente, tributário correto e forma/registro/prazo. Use como passo final obrigatório de qualquer produção imobiliária, quando o advogado digitar /revisao-final-imobiliaria, pedir "revisa antes de protocolar/assinar", "confere se está tudo certo", "faz o pente-fino", ou quando outra skill de peça encaminhar para revisão. Reprova lei revogada, ITBI errado, prazo decadencial perdido e citação de jurisprudência não ancorada.
---

# suprema-corte-imobiliaria — auditoria R1-R4

Revisor final. Nenhuma peça/contrato/parecer imobiliário sai sem passar pelas 4 rodadas. Para cada rodada: **liste o que checou, o achado e o veredito** (✅ ok · 🟠 corrigir · 🔴 bloqueia). Só entrega com R1-R4 verdes. Trabalha junto de `validador-imobiliario` (cruza cada âncora com `context/`) e do guard `anti-alucinacao-imobiliaria`.

## R1 — Fatos, partes, imóvel e matrícula
- **Imóvel identificado sem ambiguidade:** matrícula nº + cartório (RI), descrição/confrontações, nº de contribuinte/IPTU. Bate com `memoria-de-caso-imobiliario`?
- **Cadeia dominial:** quem consta como proprietário **no registro** é o vendedor/réu? (só o registro transfere — CC art. 1.245). Concentração conferida (Lei 13.097/2015 art. 54)?
- **Partes e capacidade:** qualificação completa; **outorga conjugal** quando exigível (CC art. 1.647); espólio/inventariante; representação de PJ.
- **Confrontantes e terceiros:** em usucapião/demarcatória, todos os confinantes e titulares foram indicados/citados (CPC art. 246, §3º)?
- **Prova dos fatos:** cada afirmação tem documento? (matrícula, contrato, recibos, notificação de mora, ata de assembleia).

## R2 — Fundamentação VIGENTE (nunca lei revogada)
- **Lei atual manda.** Reprovar redação revogada. Conferir as reformas: Marco das Garantias (Lei 14.711/2023), SERP (Lei 14.382/2022), Distrato (13.786/2018), Taxa Legal (**Lei 14.905/2024** — arras art. 418 CC; juros/correção = **SELIC-IPCA**, não "1% a.m.").
- **Registral:** silêncio do confinante na usucapião extrajudicial = **concordância desde a Lei 13.465/2017** (não "novidade 2026"); adjudicação extrajudicial = art. 216-B (independe de registro prévio, §2º).
- **Fiduciária/hipoteca:** Lei 9.514 + Marco 14.711/2023 (consolidação, purga, leilão 60d, 2º leilão aceita metade da avaliação, AF sucessiva/superveniente, **26-A residencial exonera saldo**); hipoteca com **execução extrajudicial no RI**. AF segue a Lei 9.514, não o CDC (Tema 1.095 STJ).
- **Toda jurisprudência ancorada:** cada súmula/tema citado existe em `context/jurisprudencia-imobiliaria.md` com número correto? (ex.: **REsp** 1.937.821, não RE). Sem âncora → 🔴.
- **Postura honesta nos rachas:** Súmula 308 × AF (4ª Turma nega); Tema 796 × holding; retenção 50% distrato (CC art. 413); LC 227 × Tema 1.113. A peça reconhece a divergência em vez de prometer vitória?

## R3 — Tributário correto
- **ITBI base:** valor de mercado **declarado na transação** (Tema 1.113 STJ), não vinculado ao IPTU nem a "valor de referência" unilateral do município (art. 148 CTN). Cobrança a maior → defesa administrativa/restituição.
- **ITBI momento:** fato gerador = **registro** da transmissão (não a promessa).
- **Imunidade:** integralização de capital é imune **só até o limite do capital social** (Tema 796 STF); excedente tributa. Holding com atividade preponderante imobiliária = campo em disputa — não prometer imunidade automática.
- **Tensão LC 227/2026** (tentou reabilitar estimativa fiscal por critérios técnicos + contraditório diferido): sinalizar como **tese**, não vitória garantida.
- **Locação não é só IR:** desde 2026 entra em **IBS/CBS** (LC 214/2025) — parecer/consultivo deve considerar (cross-link `tributario-societario`).
- Distinguir do **ITCMD** (doação/herança → `tributario-societario`/`familia`).

## R4 — Forma, registro e prazo
- **Forma do ato:** exige **escritura pública** (CC art. 108 — imóvel > 30 salários mínimos)? Exceções por instrumento particular: **Lei 9.514 art. 38** (SFI/AF) e **SFH** (Lei 4.380). Contrato particular sem essas exceções para imóvel de alto valor → 🔴.
- **Registro para eficácia:** compromisso irretratável registrado gera direito real (CC 1.417) e título executivo (CPC 784 III); convenção de condomínio precisa de registro para oponibilidade a terceiros (2/3 — CC 1.333/1.334); instituição registrada (CC 1.332).
- **Prazos fatais:** **renovatória** (interstício **1 ano a 6 meses** antes do fim do contrato — decadência); revisional só **após 3 anos** (art. 19); **purga da mora** na locação **15 dias da citação**, vedada se usada nos **24 meses**; distrato conforme data do contrato.
- **Competência e valor da causa:** foro da **situação do imóvel** para direito real/possessória; valor da causa correto.
- **Pedido completo:** liminar/tutela requerida quando cabível; averbação/registro da decisão pedido quando for o caso.

## Veredito final
Só entregue com **R1 ✅ · R2 ✅ · R3 ✅ · R4 ✅**. Qualquer 🔴 devolve à skill de origem com a correção pontual. Registre o resultado em `memoria-de-caso-imobiliario`.
