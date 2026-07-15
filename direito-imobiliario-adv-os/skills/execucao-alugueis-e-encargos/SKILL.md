---
name: execucao-alugueis-e-encargos
description: "Estrutura a cobranca e a execucao de alugueis e encargos vencidos (contrato escrito de locacao = titulo executivo extrajudicial, credito de aluguel do CPC art. 784), a acao de cobranca quando o titulo nao basta, e a consignacao de aluguel/chaves quando o locador se recusa a receber, aplicando o art. 58 (foro do imovel, valor da causa 12 meses) e a possibilidade de a cobranca correr antes da desocupacao (art. 62). Use quando o operador disser: executar alugueis atrasados, cobrar aluguel e encargos, execucao do contrato de locacao, acao de cobranca de aluguel, consignar aluguel, consignacao das chaves, deposito do aluguel em juizo."
---

# EXECUCAO DE ALUGUEIS E ENCARGOS (Lei 8.245/91 c/c CPC)

> Camada 5 — Locacao. Recuperacao do credito locaticio e consignacao. Anexos: `context/lei-8245-locacao.md`.

## Quando ativa
Locador quer receber alugueis/encargos vencidos (com ou sem despejo); OU locatario quer se liberar da mora consignando aluguel ou entregando as chaves recusadas.

## Base legal ancorada
- **Titulo executivo (✅/ 🟡 inciso):** o contrato de locacao **escrito** e titulo executivo extrajudicial (CPC art. 784 — credito decorrente de aluguel de imovel e encargos), viabilizando **execucao** direta dos alugueis e encargos, sem fase de conhecimento. 🟡 *Confirmar o inciso exato do art. 784 no `validador-imobiliario`/`context/` antes de citar em peca.* Sem contrato escrito ou havendo iliquidez, vai-se pela **acao de cobranca** (rito comum).
- **Art. 58 — disposicoes processuais comuns (✅):** foro do lugar do imovel (salvo eleicao); **valor da causa = 12 meses de aluguel**; citacao/notificacao por AR se autorizada no contrato; recursos so com efeito devolutivo; tramita em ferias forenses. Aplicam-se subsidiariamente CC e CPC (art. 79).
- **Art. 62 (✅):** cabe **cumular** a cobranca com o despejo por falta de pagamento; a **execucao da cobranca pode iniciar antes da desocupacao** (a cobranca nao depende de o inquilino ter saido). Fiadores sao citados para a cobranca.
- **Consignacao (✅):** consignacao de **aluguel e encargos** (recusa do locador em receber) e consignacao das **chaves** seguem o rito da lei c/c CPC (acao consignatoria) — libera o locatario da mora e faz cessar os alugueis a partir do deposito valido das chaves.

## O que produzir
**Se for cobranca/execucao (locador):**
1. Escolher a via: **execucao** (contrato escrito = titulo, CPC art. 784, credito de aluguel) x **acao de cobranca** (sem titulo liquido/certo).
2. **Discriminar o debito:** alugueis vencidos, encargos (IPTU/condominio conforme contrato), multa moratoria, juros e correcao — memoria de calculo (SELIC-IPCA, Lei 14.905/2024).
3. Incluir **fiadores/garantidores** no polo passivo (fianca), observando a extensao da garantia (arts. 39/40).
4. Foro do imovel; valor da causa = 12 alugueis (art. 58).
5. Se cumular com despejo, requerer o processamento conjunto (art. 62) e a continuidade da cobranca ainda que desocupado.

**Se for consignacao (locatario):**
1. Demonstrar a **recusa** (ou mora accipiendi) do locador em receber aluguel/encargos ou as chaves.
2. Depositar o valor integral (ou entregar as chaves) em juizo; requerer a declaracao de quitacao/cessacao dos alugueis a partir do deposito.
3. Alertar: a consignacao das chaves faz cessar os alugueis so a partir do **deposito valido** — atraso na entrega mantem a locacao viva.

## Postura honesta
- A **cobranca corre independentemente do despejo** — nao condicionar o recebimento a desocupacao (art. 62).
- Sem contrato escrito, **nao ha execucao** direta: e cobranca pelo rito comum (mais lenta) — dizer isso ao operador.
- O **fiador** so responde nos limites da garantia a que anuiu (ver `locacao-defesa-e-fiador`) — nao presumir responsabilidade ilimitada na prorrogacao.

## Cross-link soft (nao duplicar)
- Rito e atos de execucao/cumprimento (penhora, expropriacao, embargos) -> `execucao` e `cumprimento-e-execucao-imobiliaria`.
- Memoria de calculo do debito -> `calculosjudiciais`.
- Despejo por falta de pagamento e purga da mora -> `acao-despejo` e `locacao-defesa-e-fiador`.

## Guard
Nenhum dispositivo sem `validador-imobiliario`; guard `anti-alucinacao-imobiliaria` (titulo CPC art. 784 — confirmar inciso; art. 58 valor 12 meses; cobranca antes da desocupacao). Entrega pela `suprema-corte-imobiliaria` (R1-R4).
