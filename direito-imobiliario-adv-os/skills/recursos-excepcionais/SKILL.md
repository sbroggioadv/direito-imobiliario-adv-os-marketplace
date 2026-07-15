---
name: recursos-excepcionais
description: "Redige recurso especial (CPC 1.029 + CF 105 III) e extraordinario (CF 102 III) em causa imobiliaria e faz o juizo de admissibilidade/tempestividade completo antes de interpor — prequestionamento obrigatorio, repercussao geral no RE (1.035), repetitivos (1.036-1.041), preparo/desercao (1.007), prazo 15 dias uteis e a barreira do reexame de prova (Sumula 7/STJ e Sumula 279/STF — posse, tempo de posse, boa-fe e valor de mercado sao FATO). Use quando o operador disser REsp, recurso especial, RE, recurso extraordinario, repercussao geral, repetitivo, prequestionamento, esse recurso e cabivel?, vai ser conhecido?, levar pro STJ/STF."
---

# RECURSOS-EXCEPCIONAIS — REsp / RE + Admissibilidade

> Camada 8 (recursos). **Standalone** — CPC inline. Via estreita: so questao de **direito**, prequestionada. Sem prequestionamento ou querendo reexame de prova, nao conhece.

## Anexos e skills de apoio
- `context/jurisprudencia-imobiliaria.md` (ancoras que sobem: ITBI Tema 1.113/REsp 1.937.821, imunidade Tema 796, AF Tema 1.095, fiador Tema 1.127; Sumula 7 STJ; Sumula 98 STJ).
- Prequestionamento em `embargos-de-declaracao`; ancoras em `jurisprudencia-imobiliaria`; validacao em `validador-imobiliario`.

## Objetivo
Levar a questao de **direito** ao STJ/STF com cabimento, prequestionamento e (no RE) repercussao geral demonstrados, tempestivo e preparado — OU emitir parecer de (in)admissibilidade antes de interpor.

## Quando ativar
- Causa imobiliaria decidida em ultima/unica instancia que contrarie **lei federal/tratado ou divirja** (REsp) ou contrarie a **CF** (RE).
- Gate de admissibilidade: "esse recurso e cabivel?", "vai ser conhecido?", "checar preparo/desercao".
- Gatilhos: "REsp", "recurso especial", "RE", "repercussao geral", "repetitivo", "prequestionar", "STJ/STF".

## Metodologia
1. **Cabimento:** **REsp** (CF 105 III + CPC 1.029) — contrariedade a lei federal/tratado (ex.: CC 1.245, Lei 9.514, Lei 8.245, LRP 216-A/216-B), validade de ato local contestado, ou divergencia jurisprudencial. **RE** (CF 102 III) — contrariedade a CF (ex.: ITBI e Tema 1.113/796; funcao social). Interpor em **peticoes distintas** (1.029).
2. **🔴 BARREIRA DO REEXAME DE PROVA — Sumula 7/STJ e Sumula 279/STF:** o STJ/STF **nao reexamina fato/prova**. Em imobiliario isso barra: **tempo e caracteristicas da posse** (usucapiao), **boa-fe** do adquirente, **valor de mercado** declarado no ITBI, **existencia de esbulho**. So sobe se a controversia for de **qualificacao juridica** do fato incontroverso (revaloracao) — NAO de reexame. Enquadrar a tese como questao de direito, nunca pedir "reanalise das provas". So via `validador-imobiliario`.
3. **Prequestionamento:** a materia tem de ter sido **decidida** no acordao. Se omisso, opor **ED** antes (Sumula 98/STJ — ED prequestionador nao e protelatorio; 1.025 — prequestionamento ficto). Sem prequestionamento -> nao conhecimento. Cross-link `embargos-de-declaracao`.
4. **Divergencia (REsp — 1.029 §1):** provar o dissidio por **cotejo analitico** (acordao paradigma + similitude fatica).
5. **Repercussao geral (RE — 1.035):** o STF nao conhece RE sem RG; demonstra-la em preliminar formal (§3: ha RG se contraria sumula/jurisprudencia dominante do STF ou reconhece inconstitucionalidade de tratado/lei).
6. **Tempestividade:** **15 dias uteis** (1.003 §5), dobro por sujeito. Feriado local (1.003 §6): comprovar; nao comprovacao NAO e intempestividade automatica em regra — classificar **SANAVEL** e confirmar via `validador-imobiliario`.
7. **Preparo:** sim, sob pena de desercao (1.007). Base = valor da causa.
8. **Repetitivos (1.036-1.041):** verificar se a questao esta **afetada** (suspensao nacional — 1.037 II) ou ja tem **tese fixada** (1.040). Se desfavoravel, tentar **distinguishing** (1.037 §9); se favoravel, invocar a tese.
9. **Admissibilidade na origem (1.030):** o presidente/vice pode negar seguimento, sobrestar, devolver para retratacao ou admitir. Da negativa por RG/repetitivo (I e III) cabe **agravo interno (1.021)**; da inadmissao do inciso V cabe **agravo do 1.042** — encaminhar a `agravos-excepcionais`.
10. Redigir: enderecamento ao **presidente/vice do tribunal de origem** + cabimento + prequestionamento + (RE) repercussao geral + razoes.

## Entrega obrigatoria final
- REsp e/ou RE redigidos (peticoes distintas) com cabimento, prequestionamento demonstrado, superacao da Sumula 7/279 (tese de direito) e (no RE) preliminar de repercussao geral — OU parecer **ADMISSIVEL/INADMISSIVEL/SANAVEL** com o que sanar.
- Parecer de tempestividade + preparo + nota sobre afetacao/tese de repetitivo aplicavel.

## Guard
Toda tese/sumula/tema so via `validador-imobiliario`; ancoras em `jurisprudencia-imobiliaria`; guard `anti-alucinacao-imobiliaria`. Sem prequestionamento ou pedindo reexame de prova = risco de nao conhecimento — avisar e indicar ED previo/reenquadramento. Feriado local nao comprovado = SANAVEL, nunca perda automatica. Entrega final pela `suprema-corte-imobiliaria`.
