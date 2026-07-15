---
name: cobranca-cotas-condominiais
description: Cobra ou defende cotas condominiais atrasadas — natureza propter rem, quem responde (vendedor × comprador), penhora do bem de família e multa de 2%. Use quando o advogado pedir "cobrar cotas condominiais atrasadas", "ação de cobrança de condomínio", "execução de cotas", "quem paga o condomínio, o antigo ou o novo dono?", "dá pra penhorar o apartamento do devedor?", "penhora bem de família por condomínio", "Súmula 486 serve?", "multa de condomínio".
---

# Cobrança de Cotas Condominiais

## Quando ativa
Condomínio quer receber cotas em atraso, **ou** defesa do condômino/adquirente cobrado. Trilha condomínio (contencioso/execução). A estrutura que gera a exigibilidade da cota (instituição + convenção registradas) está em `instituicao-e-convencao-condominio`; a atualização do débito em `calculosjudiciais`; a execução do título em `execucao`.

## Base legal ancorada
- **Natureza *propter rem* — CC art. 1.345 (✅)** — a dívida de cotas **segue o imóvel**: o adquirente responde pelos débitos **anteriores** à aquisição (com direito de regresso). O imóvel é a garantia natural.
- **Legitimidade — Tema 886/STJ (REsp 1.345.331/RS, Rel. Min. Luis Felipe Salomão, 2ª Seção, repetitivo, ✅):**
  - **(a)** o que define a responsabilidade **não é o registro do compromisso**, mas a **relação jurídica material com o imóvel** (imissão na posse do promissário comprador + ciência inequívoca do condomínio sobre a transação);
  - **(b)** havendo compromisso **não registrado**, a cobrança pode recair sobre o **promitente vendedor** OU o **promissário comprador**, conforme as circunstâncias do caso.
  - A 2ª Seção **reafirmou em 2025** a natureza *propter rem* e a legitimidade passiva concorrente.
- **Multa moratória — CC art. 1.336 §1º (✅)** — multa por inadimplemento das cotas limitada a **2%** sobre o débito.
- **Penhora do bem de família — Lei 8.009/90 art. 3º, IV (✅)** — a impenhorabilidade do bem de família **NÃO se aplica** à cobrança de impostos, taxas e **contribuições devidas em função do imóvel** — aí incluída a **cota condominial**. O próprio imóvel bem de família **responde** pela dívida de condomínio.
- **Juros/correção legais = SELIC-IPCA (Lei 14.905/2024, ✅)** — não usar "1% ao mês" como default na atualização do débito.

## Postura honesta — a correção que evita o erro clássico
- 🔴 **A Súmula 486/STJ NÃO trata de cota condominial.** O enunciado real é: *"É impenhorável o único imóvel residencial do devedor que esteja locado a terceiros, desde que a renda da locação seja revertida à subsistência/moradia da família."* — é regra de **bem de família locado**, não de penhora por condomínio. Quem cita a Súmula 486 para justificar a penhora por cota **erra a fonte**. O fundamento correto é a **Lei 8.009/90 art. 3º, IV**.

## O que produzir
**Na cobrança (condomínio):**
1. **Legitimidade passiva** — definir quem cobrar pela relação material com o imóvel (Tema 886): proprietário registral, promissário comprador imitido na posse com ciência do condomínio, ou ambos. Provar a posse/ciência quando o compromisso não é registrado.
2. **Prova do débito** — convenção registrada + atas de assembleia que aprovaram as despesas ordinárias/extraordinárias + demonstrativo/planilha do débito por competência.
3. **Cálculo** — principal + correção (SELIC-IPCA, Lei 14.905/2024) + **multa 2% (art. 1.336 §1º)** + juros. Cross-link `calculosjudiciais`.
4. **Via** — cobrança/execução com base no crédito documentado na convenção e nas atas; requerer, se necessário, a **penhora do próprio imóvel** (Lei 8.009 art. 3º IV afasta o bem de família). Execução do título → `execucao`.
5. Pedido de honorários e custas.

**Na defesa (condômino/adquirente):**
- Discutir **legitimidade** (Tema 886 — quem tinha a relação material no período cobrado); questionar cotas de período anterior à posse quando havia outro responsável; conferir **quórum de aprovação** das despesas extraordinárias; **excesso de multa** (teto 2%, art. 1.336 §1º); erro de cálculo/atualização.
- Não invocar a Súmula 486 como escudo contra a penhora por cota — não se aplica.

## Cross-link (soft)
`instituicao-e-convencao-condominio` (origem da exigibilidade — propter rem depende da instituição registrada) · `execucao` (execução do título) · `calculosjudiciais` (atualização SELIC-IPCA + multa) · `civel` (rito processual) · `constituicao-associacoes` (se for "taxa" de associação, e não cota de condomínio, muda tudo — Tema 492).

## Revisão final
Fechar a peça pela `suprema-corte-imobiliaria` (R1 partes/imóvel/período do débito · R3 cálculo/atualização correta · R4 legitimidade Tema 886 e teto da multa) e `validador-imobiliario` antes de protocolar.
