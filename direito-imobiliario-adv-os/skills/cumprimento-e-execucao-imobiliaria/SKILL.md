---
name: cumprimento-e-execucao-imobiliaria
description: Fase de satisfação no imobiliário — cumprimento de sentença (obrigação de fazer/entregar/quantia) e execução de título extrajudicial imobiliário. Use quando o advogado precisar "executar o que ganhou" num caso de imóvel: outorga forçada de escritura, imissão/reintegração na posse por mandado, execução de aluguéis e encargos, cobrança de cotas condominiais, honrar título executivo (promessa com 2 testemunhas), ou dúvidas sobre como transformar a sentença/contrato imobiliário em resultado prático.
---

# Cumprimento e execução imobiliária

Transforma o **título** (sentença ou instrumento) em **resultado** — escritura registrada, posse entregue, dinheiro pago. Aqui o imobiliário tem particularidades; a máquina genérica de execução de quantia fica no plugin `execucao` (aponte, não duplique).

## 1. Primeiro passo: identifique o título e a obrigação
| Título | Obrigação | Via |
|--------|-----------|-----|
| Sentença de adjudicação / que supre a vontade | **fazer** (outorgar escritura) | cumprimento — a sentença **produz os efeitos da declaração não emitida** (**CPC 501** ✅); serve de título para registro |
| Sentença possessória/reivindicatória | **entregar coisa** (posse) | cumprimento — **mandado de imissão/reintegração** na posse |
| Sentença/acordo de quantia | **pagar** | cumprimento de quantia (rito do CPC — ver `execucao`/`calculosjudiciais`) |
| Promessa/contrato com **2 testemunhas** | título executivo extrajudicial (**CPC 784, III** ✅) | execução |
| Contrato de locação + encargos | **execução de aluguéis e encargos** (Lei 8.245 c/c CPC ✅) | execução (pode iniciar antes da desocupação — art. 62, VI ✅) |

## 2. Obrigação de fazer — outorga forçada de escritura
- Sentença de adjudicação compulsória / que supre a declaração de vontade: pelo **CPC 501** ✅, a própria sentença vale como título e se leva ao **Registro de Imóveis**. Não precisa "obrigar" o vendedor a comparecer — o juiz supre.
- Cheque **ITBI pago** (fato gerador no registro — CC 1.245 ✅; base = valor de mercado declarado, Tema 1.113 ✅) e certidões antes de levar a registro.
- **Súmula 239 STJ** ✅ — a adjudicação **independe de registro prévio** do compromisso.
- Antes de judicializar, avalie a via **extrajudicial** (art. 216-B LRP ✅) — cross-link `adjudicacao-compulsoria-extrajudicial`.

## 3. Obrigação de entregar coisa — posse
- Sentença possessória/reivindicatória/de despejo: cumpre-se por **mandado** (imissão/reintegração/desocupação). No despejo, prazo de **30 dias** (ou **15** nas hipóteses do §1º) — art. 63, Lei 8.245 ✅.
- **Execução provisória do despejo** exige **caução de 6 a 12 meses** de aluguel (art. 64 ✅). Deferida a posse ao autor, module retenção por benfeitorias do réu.

## 4. Obrigação de pagar — quantia (imobiliário)
- **Aluguéis e encargos:** execução com base no contrato + planilha (Lei 8.245 + CPC ✅); citar locatário **e fiadores**; a cobrança pode correr antes da desocupação (art. 62, VI ✅). Bem de família do fiador é **penhorável, resid. E comercial** (**Tema 1.127 STF + Súmula 549 STJ** ✅).
- **Cotas condominiais:** dívida **propter rem** (CC 1.345 ✅); o próprio imóvel bem de família responde (Lei 8.009/90, **art. 3º, IV** ✅); penhora do próprio bem em cobrança.
- **Retenção/distrato:** delimite pela data do contrato (Súmula 543 pré-2018; Lei 13.786 pós; mitigação 50%→25% por CC 413 ✅) e mande a conta para `calculosjudiciais`.
- Máquina genérica de quantia (multa e honorários após o prazo, penhora, avaliação, expropriação): **use `execucao`** — não reescreva aqui.

## 5. Penhora e expropriação de imóvel (o que é próprio do domínio)
- **Só o registro transfere** (CC 1.245 ✅) e a **concentração na matrícula** (Lei 13.097/2015, art. 54 ✅) governam a oponibilidade — averbe a penhora na matrícula para proteger a arrematação (contra fraude à execução: **Súmula 375 STJ** ✅; exceção fiscal art. 185 CTN + Tema 290 ✅).
- Havendo **garantia real**: hipoteca hoje executa **extrajudicialmente no RI** (Marco 14.711/2023, arts. 9-12 ✅) e a **alienação fiduciária** segue o rito próprio da Lei 9.514 (consolidação + leilão 60d ✅) — cross-link `hipoteca-e-execucao-extrajudicial` e `alienacao-fiduciaria-imovel`.

## 6. Cross-link soft (não duplicar)
`execucao` (rito geral de execução/cumprimento de quantia, penhora, embargos) · `calculosjudiciais` (memória de cálculo, SELIC-IPCA, retenção, aluguéis) · `civel` (fase de cumprimento no CPC) · `bancario` (veículo, DL 911).

## 7. Fechamento obrigatório
Peça (cumprimento/execução/embargos) revisada por **`suprema-corte-imobiliaria`** (R1-R4) + **`validador-imobiliario`**. Guard `anti-alucinacao-imobiliaria` ativo — dispositivo/tema só com âncora em `context/`.
