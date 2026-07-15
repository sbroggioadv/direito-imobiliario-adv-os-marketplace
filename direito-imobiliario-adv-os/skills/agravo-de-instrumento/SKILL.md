---
name: agravo-de-instrumento
description: "Redige agravo de instrumento (CPC 1.015-1.020) contra decisao interlocutoria em causa imobiliaria — liminar possessoria (562), despejo liminar (Lei 8.245 art. 59 §1), consolidacao/leilao na alienacao fiduciaria, tutela de urgencia, gratuidade, IDPJ — com pecas obrigatorias (1.017), comunicacao ao juizo (1.018), efeito suspensivo/tutela recursal (1.019 I) e taxatividade mitigada (Tema 988 STJ), prazo 15 dias uteis. Use quando o operador disser agravo de instrumento, agravar a interlocutoria, recorrer da liminar, sustar leilao fiduciario, decisao interlocutoria, efeito suspensivo no agravo, Tema 988."
---

# AGRAVO-DE-INSTRUMENTO — CPC 1.015-1.020

> Camada 8 (recursos). Recurso contra interlocutoria. **Standalone** — CPC inline. Falha em peca obrigatoria ou foro errado = nao conhecimento.

## Anexos e skills de apoio
- `context/jurisprudencia-imobiliaria.md` (Tema 988/STJ — taxatividade mitigada; ancoras).
- Base processual em `base-processual-imobiliaria`; tutelas em `tutelas-imobiliarias`; validacao em `validador-imobiliario`.

## Objetivo
Atacar a interlocutoria cabivel com instrumento completo, no prazo, com pedido de efeito suspensivo/tutela recursal bem fundamentado.

## Quando ativar
- Decisao interlocutoria do **rol do 1.015** (ou fase de liquidacao/cumprimento/execucao/inventario — par. unico).
- Cenarios imobiliarios tipicos: (des)concessao de **liminar possessoria** (562), **despejo liminar** (Lei 8.245 art. 59 §1 — 8 fundamentos + caucao 3 meses), decisao que autoriza/nega **sustacao de leilao fiduciario**, tutela de urgencia (registro/averbacao, sustacao de obra), gratuidade (V), exibicao de documento/matricula (VI), IDPJ (IV).
- Interlocutoria fora do rol com **urgencia/inutilidade do julgamento na apelacao** (Tema 988).
- Gatilhos: "agravo de instrumento", "agravar", "recorrer da liminar", "sustar leilao", "efeito suspensivo", "Tema 988".

## Metodologia
1. **Cabimento (1.015):** conferir se a materia esta no rol (I tutelas provisorias; II merito; III arbitragem; IV IDPJ; V gratuidade; VI exibicao; VII exclusao de litisconsorte; VIII limitacao do litisconsorcio; IX intervencao de terceiros; X efeito suspensivo a embargos a execucao; XI redistribuicao do onus da prova; XIII outros em lei) + par. unico.
2. **Fora do rol — Tema 988/STJ:** taxatividade **mitigada** — cabe AI se demonstrada **urgencia decorrente da inutilidade do julgamento da questao na apelacao**. Sem isso, a interlocutoria nao-agravavel vai em **preliminar de apelacao ou contrarrazoes** (1.009 §1) — registrar a ressalva. Tese so via `validador-imobiliario`.
3. **Tempestividade:** **15 dias uteis** (1.003 §5), dobro por sujeito. Feriado local (1.003 §6) = SANAVEL se nao comprovado.
4. **Pecas obrigatorias (1.017, I):** inicial, contestacao, peticao que ensejou a decisao, **decisao agravada**, certidao de intimacao (ou prova de tempestividade) e **procuracoes**. **§5: dispensadas em autos eletronicos.** Falta de peca -> relator intima para sanar (932 par. unico).
5. **Comunicacao ao juizo de 1o grau (1.018):** em **autos fisicos**, juntar copia do agravo na origem em **3 dias** (§2); descumprimento arguido e provado -> inadmissibilidade (§3). Em autos eletronicos, dispensado.
6. **Efeito suspensivo / tutela recursal (1.019, I):** fundamentar **probabilidade de provimento + risco de dano** — o relator decide em 5 dias. Em **sustacao de leilao fiduciario** e **despejo liminar**, este e o pedido central (o dano da perda da posse/propriedade e concreto).
7. **Preparo:** custas + porte quando devidos (1.017 §1). Base = valor da causa.
8. Redigir: enderecamento ao **tribunal** + razoes (reforma/invalidacao) + pedido de efeito suspensivo + nomes/enderecos dos advogados (1.016).

## Entrega obrigatoria final
- Agravo redigido + **lista das pecas obrigatorias do 1.017** (ou nota de dispensa em autos eletronicos) + minuta da comunicacao do 1.018 se autos fisicos.
- Parecer de tempestividade + cabimento (rol ou Tema 988) + pedido de efeito suspensivo/tutela recursal fundamentado.

## Guard
Tese (Tema 988) so via `validador-imobiliario`; ancoras em `jurisprudencia-imobiliaria`; guard `anti-alucinacao-imobiliaria`. Fora do rol sem urgencia/inutilidade demonstrada = risco de nao conhecimento — avisar e oferecer a via da preliminar de apelacao. Entrega final pela `suprema-corte-imobiliaria`.
