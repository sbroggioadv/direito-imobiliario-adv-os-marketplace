---
name: acao-despejo
description: "Redige acao de despejo pelo fundamento correto e busca a liminar de desocupacao em 15 dias (art. 59 §1º — 8 fundamentos, mediante caucao de 3 meses de aluguel) ou o despejo por falta de pagamento com purga da mora (art. 62 — 15 DIAS DA CITACAO, vedada se ja usada nos 24 MESES), com mandado do art. 63 (30/15 dias) e execucao provisoria do art. 64 (caucao 6-12 meses). Use quando o operador disser: acao de despejo, despejo por falta de pagamento, retomada do imovel, despejo liminar, denuncia vazia, purga da mora no despejo, desocupar inquilino."
---

# ACAO DE DESPEJO (arts. 59-66, Lei 8.245/91)

> Camada 5 — Locacao. Peca inicial de retomada. Anexos: `context/lei-8245-locacao.md`.

## Quando ativa
Locador quer retomar o imovel: fim de prazo, denuncia (vazia/cheia), falta de pagamento, infracao contratual/legal, fim de garantia.

## Base legal ancorada
- **Art. 59 — rito comum + LIMINAR de desocupacao em 15 dias (✅)** *inaudita altera parte*, mediante **caucao de 3 meses de aluguel**, nos fundamentos EXCLUSIVOS do §1º (**9 incisos, I a IX** — VI a IX incluidos pela Lei 12.112/09):
  - **I** — descumprimento de acordo escrito (2 testemunhas, prazo min. 6 meses);
  - **II** — extincao de contrato de trabalho;
  - **III** — fim de locacao de temporada (acao em ate 30 dias);
  - **IV** — morte do locatario sem sucessor legitimo;
  - **V** — permanencia de sublocatario apos extincao;
  - **VI** — reparacoes urgentes do Poder Publico recusadas;
  - **VII** — fim do prazo do art. 40, p.u. sem nova garantia;
  - **VIII** — fim da locacao **NAO residencial** (acao em ate 30 dias do termo/notificacao) — porta do despejo liminar do ponto comercial.
  - **IX** — **falta de pagamento** de aluguel e acessorios no vencimento **estando o contrato SEM qualquer das garantias do art. 37** (por nao ter sido contratada, ou por extincao/exoneracao dela) — liminar de despejo por inadimplemento quando nao ha garantia.
- **Art. 62 — despejo por falta de pagamento + PURGA DA MORA (✅, red. 12.112/09):**
  - Cabe cumular rescisao + cobranca; cita-se o locatario para a rescisao e **locatario e fiadores** para a cobranca.
  - **Purga da mora: prazo de 15 dias contados da CITACAO** (inclui alugueis vincendos ate a efetivacao, multas, juros, custas e honorarios de 10%). 🔴 *NAO e "no prazo da contestacao" (redacao antiga revogada).*
  - **Paragrafo unico:** vedada a emenda da mora se ja usada nos **24 MESES** anteriores. 🔴 *Sao 24 meses, NAO "2x em 12 meses".*
- **Art. 63 (✅, red. 12.112/09):** julgado procedente, expede-se **mandado de despejo com 30 dias** para desocupacao voluntaria; cai para **15 dias** nas hipoteses do §1º.
- **Art. 64 (✅, red. 12.112/09):** execucao provisoria do despejo (salvo art. 9º) exige **caucao de 6 a 12 meses** de aluguel.
- **Art. 58 (✅):** foro do lugar do imovel (salvo foro de eleicao); **valor da causa = 12 meses de aluguel**; **recursos so com efeito devolutivo** (sentenca executa provisoriamente); tramita em ferias forenses.

## O que produzir (estrutura da inicial)
1. **Enquadrar o fundamento** — verificar se cabe liminar do art. 59 §1º (8 incisos taxativos) ou se e denuncia vazia (art. 46, prorrogado indeterminado) / cheia (art. 47) / falta de pagamento (art. 62).
2. **Competencia/valor:** foro do imovel; valor da causa = 12 alugueis (art. 58, III).
3. **Pedido de liminar** (se cabivel): oferecer caucao de 3 meses; requerer desocupacao em 15 dias inaudita altera parte.
4. **Cumulacao rescisao + cobranca** (falta de pagamento): citar locatario para rescisao e locatario+fiadores para cobranca; discriminar o debito (alugueis, encargos, multa, juros).
5. **Notificacao previa** quando o fundamento exigir (fim de garantia art. 40 p.u.; denuncia; nao residencial).
6. **Pedidos:** rescisao, despejo com prazo do art. 63, condenacao no debito e encargos ate a desocupacao, honorarios.
7. Se for executar provisoriamente a sentenca: prever caucao de 6-12 meses (art. 64).

## Postura honesta
- **Rol do art. 59 §1º e taxativo** — fora dos 8 incisos, nao ha liminar; o despejo segue o rito comum sem desocupacao antecipada.
- **Purga da mora e direito do locatario** (art. 62, II) e so e vedada se usada nos **24 meses** — nao prometer despejo rapido em falta de pagamento sem checar esse historico.
- Sumulas 1 e 2 do STJ (foro do imovel / purga ate a sentenca) tem teor consolidado mas **nao foram abertas em fonte oficial** nesta base — ancorar na **letra dos arts. 58 e 62**, nao na sumula, ate confirmacao.

## Cross-link soft (nao duplicar)
- Defesa do locatario/fiador, purga e exoneracao -> `locacao-defesa-e-fiador`.
- Cobranca/execucao do debito de alugueis e consignacao -> `execucao-alugueis-e-encargos`.
- Calculo do debito (SELIC-IPCA, Lei 14.905/2024) -> `calculosjudiciais`.

## Guard
Nenhum dispositivo sem `validador-imobiliario`; guard `anti-alucinacao-imobiliaria` (purga 15d da citacao, vedacao 24 meses, caucoes 3/6-12 meses). Entrega pela `suprema-corte-imobiliaria` (R1-R4).
