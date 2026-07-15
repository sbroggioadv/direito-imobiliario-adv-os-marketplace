---
name: revisional-de-aluguel
description: "Redige acao revisional de aluguel para ajustar o valor ao preco de mercado apos 3 anos de vigencia (art. 19), com pedido de fixacao de aluguel provisorio ja na inicial (art. 68 — ate 80% do pedido para o locador; nao inferior a 80% do vigente para o locatario). Use quando o operador disser: acao revisional de aluguel, revisar valor do aluguel, reajustar aluguel a mercado, aluguel provisorio, aluguel defasado, atualizar o valor da locacao judicialmente, revisao trienal do aluguel."
---

# REVISIONAL DE ALUGUEL (arts. 19 e 68, Lei 8.245/91)

> Camada 5 — Locacao. Acao para reequilibrar o valor locaticio ao mercado, ajuizavel por locador OU locatario. Anexos: `context/lei-8245-locacao.md`.

## Quando ativa
Aluguel defasado (para cima ou para baixo) em relacao ao mercado, sem acordo entre as partes, apos 3 anos do contrato ou do ultimo acordo/revisao.

## Base legal ancorada
- **Art. 19 — REVISIONAL (✅):** nao havendo acordo, **locador ou locatario**, **apos 3 anos** de vigencia do contrato ou do ultimo acordo, podem pedir **revisao judicial** do aluguel para ajuste ao **preco de mercado**. E o marco trienal — antes disso, so por acordo.
- **Art. 68 — rito e ALUGUEL PROVISORIO (✅):** ja na inicial o juiz pode fixar aluguel provisorio:
  - a pedido do **locador**: ate **80% do valor pedido** na inicial;
  - a pedido do **locatario**: **nao inferior a 80% do aluguel vigente**.
  - O provisorio vigora enquanto se apura o valor de mercado (pericia/prova). Rito sumario (procedimento especial da lei c/c CPC).

## O que produzir (estrutura da inicial)
1. **Conferir o marco trienal** (art. 19): 3 anos desde o contrato ou desde o ultimo acordo/revisao — se nao completou, a acao e prematura.
2. **Provar a defasagem** ao mercado: laudo/parecer de avaliacao, comparativos de locacoes semelhantes na regiao (base para a pericia).
3. **Pedir a fixacao do aluguel provisorio** (art. 68) no patamar legal conforme quem propoe (locador ate 80% do pedido / locatario nao abaixo de 80% do vigente).
4. Pedido: fixacao do novo aluguel a mercado, com efeitos e diferencas conforme a apuracao; requerer pericia avaliatoria.
5. Competencia/valor: foro do imovel; valor da causa conforme art. 58 (12 meses da diferenca/valor pretendido).

## Postura honesta
- **Nao ha sumula nem tema repetitivo do STJ especifico sobre revisional** — regida pela **letra da Lei 8.245 (arts. 19 e 68) + precedentes esparsos**. Nao inventar enunciado.
- O **prazo trienal** e requisito de admissibilidade — proposta antes dos 3 anos tende a extincao; so o acordo antecipa a revisao.
- Revisional **nao se confunde com reajuste contratual** (indice pactuado, anual): o reajuste e automatico pela clausula; a revisional recompoe o valor real a mercado apos 3 anos.

## Cross-link soft (nao duplicar)
- Renovacao compulsoria de ponto comercial (que tambem fixa novo aluguel) -> `acao-renovatoria` (nao confundir — la o gatilho e o fim do contrato, aqui e a defasagem).
- Calculo das diferencas e atualizacao (SELIC-IPCA, Lei 14.905/2024) -> `calculosjudiciais`.

## Guard
Nenhum dispositivo sem `validador-imobiliario`; guard `anti-alucinacao-imobiliaria` (marco trienal art. 19; provisorio 80% art. 68; sem sumula propria). Entrega pela `suprema-corte-imobiliaria` (R1-R4).
