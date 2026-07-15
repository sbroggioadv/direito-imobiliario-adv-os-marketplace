---
name: agravos-excepcionais
description: "Redige o agravo interno (CPC 1.021) contra decisao MONOCRATICA do relator em causa imobiliaria (impugnacao especifica §1, multa 1-5% §4) e o agravo do CPC 1.042 contra a decisao que INADMITE REsp ou RE na origem (salvo inadmissao por repercussao geral/repetitivo, caso em que cabe agravo interno; isento de custas §2; um agravo por recurso §6), prazo 15 dias uteis. Use quando o operador disser agravo interno, decisao monocratica, decisao do relator, levar ao colegiado, agravo regimental, agravo em recurso especial/extraordinario, agravo do 1.042, REsp/RE inadmitido, nao subiu o recurso."
---

# AGRAVOS-EXCEPCIONAIS — Agravo interno (1.021) + Agravo do 1.042

> Camada 8 (recursos). **Standalone** — CPC inline. Devolve ao colegiado a monocratica do relator e destrava o REsp/RE inadmitido na origem.

## Anexos e skills de apoio
- `context/jurisprudencia-imobiliaria.md` (tese pertinente ao caso, quando houver).
- Base processual em `base-processual-imobiliaria`; via excepcional em `recursos-excepcionais`; validacao em `validador-imobiliario`.

## Objetivo
(A) Levar ao colegiado a decisao monocratica do relator, atacando cada fundamento, sem a multa do §4; (B) fazer subir o REsp/RE inadmitido na origem pela via correta.

## Quando ativar
- O **relator** decidiu **monocraticamente** (negou seguimento, deu/negou provimento, inadmitiu) e o RI permite o agravo interno.
- O presidente/vice **inadmitiu** o REsp ou RE na origem.
- Gatilhos: "agravo interno", "decisao monocratica", "decisao do relator", "levar ao colegiado", "agravo do 1.042", "REsp/RE inadmitido", "nao subiu o recurso".

## Metodologia

### A) Agravo interno — CPC 1.021
1. **Cabimento:** decisao **monocratica do relator** -> agravo ao **orgao colegiado**, conforme o **regimento interno** do tribunal. Confirmar que nao e caso de outro recurso (ED, agravo do 1.042).
2. **Tambem cabe** contra a decisao do presidente/vice nos incisos I e III do 1.030 (inadmissao de REsp/RE por **repercussao geral ou repetitivo**) — nesse ponto e a via correta, NAO o 1.042.
3. **Tempestividade:** **15 dias uteis** (1.003 §5), dobro por sujeito.
4. **Impugnacao especifica (1.021 §1):** o agravo **deve impugnar especificamente** cada fundamento da decisao agravada — peticao que so repete o recurso e inadmitida. Enfrentar ponto a ponto.
5. **Retratacao (1.021 §2):** o relator intima o agravado (15 dias) e, nao havendo retratacao, leva a julgamento. §3 veda ao relator so reproduzir a decisao agravada.
6. **Multa (1.021 §4-5):** se declarado **manifestamente inadmissivel/improcedente em votacao unanime**, multa de **1% a 5%** do valor atualizado da causa; novo recurso condicionado a **deposito previo** (salvo Fazenda e gratuidade — pagam ao final). Avaliar o risco.
7. **Preparo:** conforme o RI. Redigir: enderecamento ao **orgao colegiado** (via relator) + impugnacao especifica + pedido de provimento.

### B) Agravo do 1.042
8. **Triagem do fundamento da inadmissao (1.030):** se a inadmissao se fundou em **RG ou repetitivo** (I e III), **NAO** cabe o 1.042 — cabe **agravo interno** (item A.2). Cabe o 1.042 contra a **inadmissao do inciso V** (negativa de subida por outro motivo).
9. **Tempestividade:** **15 dias uteis** (1.003 §5), dobro por sujeito.
10. **Preparo:** o agravo do 1.042 **independe de custas e despesas postais** (1.042 §2).
11. **Interposicao conjunta (1.042 §6):** havendo RE **e** REsp inadmitidos, **um agravo para cada** recurso. Autos ao STJ primeiro, depois ao STF (§7-8).
12. Redigir: dirigido ao **presidente/vice da origem**, atacando os fundamentos da inadmissao + reafirmando o cabimento do REsp/RE.

## Entrega obrigatoria final
- Agravo interno (impugnacao especifica de cada fundamento) **ou** agravo do 1.042 (um por recurso inadmitido), com a triagem 1.042 x agravo interno explicitada.
- Parecer de tempestividade + alerta sobre a multa do 1.021 §4 (interno) e nota de isencao de preparo do 1.042 §2.

## Guard
Tese/sumula so via `validador-imobiliario`; ancoras em `jurisprudencia-imobiliaria`; guard `anti-alucinacao-imobiliaria`. Inadmissao por RG/repetitivo = via errada para o 1.042 (cabe agravo interno) — avisar e redirecionar. Impugnacao generica no interno = risco real de multa — exigir enfrentamento ponto a ponto. Entrega final pela `suprema-corte-imobiliaria`.
