---
name: protocolo-p4-imobiliario
description: Cruzamento das 4 esferas de um caso imobiliário — extrajudicial (cartório/registro), judicial, administrativo/municipal (ITBI, prefeitura, REURB) e tributário (LC 227/2026 ITBI-ITCMD, LC 214/2025 IBS-CBS). Use quando um caso de imóvel tocar mais de uma frente ao mesmo tempo, quando o advogado precisar decidir "por onde começar" e em que ordem, sequenciar cartório × ação × defesa fiscal, ou não deixar escapar a repercussão tributária/registral de uma medida. Diferencial estrutural do domínio.
---

# Protocolo P4 — cruzamento de esferas imobiliárias

Um mesmo fato do imóvel irradia em **4 esferas**. O erro caro é tratar uma só e ser surpreendido pelas outras (paga ITBI que não devia, perde a via de cartório, prescreve a defesa fiscal). Este protocolo **mapeia as 4 frentes, sequencia e evita o buraco**.

## As 4 esferas (P4)
| Esfera | Onde | O que se resolve | Âncoras |
|--------|------|------------------|---------|
| **1. Extrajudicial** (cartório/registro/notas) | RI, Tabelionato | regularizar sem ação: usucapião 216-A, adjudicação 216-B, retificação 213, dúvida 198-204, AF/hipoteca extrajudicial | Lei 14.382/2022 (SERP) ✅; Lei 14.711/2023 ✅ |
| **2. Judicial** | Foro do imóvel | litígio: possessória, usucapião judicial, reivindicatória, despejo, cobrança, defesa | CPC 558/562/501/246§3º ✅; Lei 8.245 ✅ |
| **3. Administrativa/municipal** | Prefeitura/Fisco municipal, CNJ | ITBI (lançamento/defesa), habite-se/averbação, REURB, corregedoria | Tema 1.113 ✅; Lei 13.465 (REURB) ✅ |
| **4. Tributária** | Fisco municipal e federal | ITBI/ITCMD (LC 227/2026) e IBS/CBS (LC 214/2025) da operação | LC 227/2026 ✅; LC 214/2025 ✅; Tema 796 ✅ |

## Como rodar o protocolo
1. **Fotografe o caso** nas 4 esferas — pergunte, para cada uma, "isto aqui tem frente aberta?".
2. **Escolha a porta mais barata que resolve** — extrajudicial **antes** de judicial (mais rápido, mais barato, é o fosso do plugin).
3. **Sequencie** — ordene os atos para que um não atropele o outro (ex.: recolher ITBI antes de registrar; averbar penhora antes de arrematar).
4. **Antecipe a repercussão** — toda medida numa esfera dispara efeito em outra (ver matriz abaixo).
5. **Não deixe buraco** — feche cada frente ou registre por que não se aplica.

## Matriz de repercussão (o que dispara o quê)
- **Registrar a transmissão** (esfera 1) → **gera ITBI** (esfera 3/4): fato gerador no registro (CC 1.245 ✅); base = valor de mercado declarado (Tema 1.113 ✅), **tensão LC 227/2026** (postura honesta ✅). Recolher a guia **antes** de lavrar/registrar.
- **Adjudicação** — decida a **porta**: extrajudicial (216-B LRP ✅, independe de registro prévio — Súmula 239 ✅) **ou** judicial (CC 1.418 + CPC 501 ✅). Ambas geram ITBI no registro.
- **Usucapião** — extrajudicial (216-A, silêncio do confinante = **concordância desde a Lei 13.465/2017** ✅) trava e **remete ao Judiciário** se houver impugnação **fundamentada**; a rejeição extrajudicial **não impede** a via judicial (§9º).
- **Locar** (esfera 1/2) → **IBS/CBS** (esfera 4): locação entra no IBS/CBS com **redução de 70%** (LC 214/2025 ✅); PF vira contribuinte acima do limiar (>3 imóveis + R$240k / R$288k) ✅; **regime opcional 3,65%** (art. 487, contratos até 16/01/2025 registrados até 31/12/2025) ✅. Cross-link `parecer-imobiliario`, `tributario-societario`.
- **Executar garantia real** — hipoteca hoje executa **extrajudicialmente no RI** (Marco 14.711/2023, arts. 9-12 ✅); AF segue rito próprio da Lei 9.514 (consolidação + leilão 60d ✅). A consolidação (esfera 1) exige **ITBI pago** pelo fiduciário.
- **Comprar de empresário individual** (esfera 1) → risco **fiscal** (esfera 4): fraude à execução fiscal, alienação após dívida ativa presume-se fraudulenta (**art. 185 CTN + Tema 290** ✅; Súmula 375 não se aplica). Puxar PGFN por **CPF e CNPJ**.
- **REURB** (esfera 3) → título registrável (esfera 1): legitimação fundiária = modo **originário** (art. 23, Lei 13.465 ✅); CRF registrada abre matrículas; REURB-S com gratuidade de emolumentos ✅.
- **Doação/sucessão do imóvel** → **ITCMD** (esfera 4): normas gerais na **LC 227/2026** ✅ — mandar ao `holding`/`familia`.

## Exemplo integrado (compra e venda)
DD (esfera 1 — matrícula + certidões + PGFN CPF/CNPJ) → instrumento correto (108/9.514 ✅) → **ITBI** apurado pelo valor declarado (Tema 1.113, ressalva LC 227 ✅) → escritura/registro (esfera 1) → se locar depois, **IBS/CBS** (esfera 4) → se o vendedor recusar a definitiva, **adjudicação** (216-B extrajudicial ou judicial). Cada seta é uma esfera; o P4 garante que nenhuma fique aberta.

## Cross-link soft (não duplicar)
`tributario-societario`/`holding` (planejamento, ITCMD, integralização) · `familia` (partilha/sucessão) · `execucao` (execução) · `calculosjudiciais` (contas) · `civel` (processual).

## Fechamento
Se o P4 gerar peça/parecer, feche por **`suprema-corte-imobiliaria`** (R1-R4) + **`validador-imobiliario`**. Guard `anti-alucinacao-imobiliaria` ativo — cada esfera só cita o ancorado em `context/`.
