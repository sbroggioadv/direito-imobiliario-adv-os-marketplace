---
name: embargos-de-declaracao
description: "Redige embargos de declaracao (CPC 1.022-1.026) contra qualquer decisao em causa imobiliaria (omissao, contradicao, obscuridade, erro material), prazo de 5 dias uteis, sem preparo, que INTERROMPEM o prazo do recurso principal (1.026). Cobre o prequestionamento (Sumula 98/STJ — nao protelatorio) para levar ITBI/Tema 1.113, Tema 796, alienacao fiduciaria e demais teses ao STJ/STF, e a multa do 1.026 §2-4. Use quando o operador disser embargar, embargos de declaracao, ED, omissao na sentenca/acordao, contradicao, obscuridade, erro material, prequestionar, juiz nao analisou meu pedido."
---

# EMBARGOS-DE-DECLARACAO — CPC 1.022-1.026

> Camada 8 (recursos). **Standalone** — CPC inline. Unico recurso de prazo 5 dias e sem preparo. INTERROMPE o prazo do recurso principal — porta de prequestionamento.

## Anexos e skills de apoio
- `context/jurisprudencia-imobiliaria.md` (Sumula 98/STJ — prequestionamento nao protelatorio; ancoras que sobem).
- Base processual em `base-processual-imobiliaria`; validacao em `validador-imobiliario`; via excepcional em `recursos-excepcionais`.

## Objetivo
Sanar vicio da decisao (omissao/contradicao/obscuridade/erro material) ou **prequestionar** materia federal/constitucional para a via excepcional, sem incorrer em ED protelatorio.

## Quando ativar
- A decisao tem omissao, contradicao, obscuridade ou erro material (ex.: sentenca que decreta despejo mas nao fixa caucao; acordao que silencia sobre a base de calculo do ITBI).
- Precisa **prequestionar** tese imobiliaria (ITBI Tema 1.113/REsp 1.937.821, imunidade Tema 796, AF Tema 1.095, fiador Tema 1.127) para REsp/RE.
- Gatilhos: "embargar", "ED", "o juiz nao analisou", "contradicao", "obscuro", "erro material", "prequestionar".

## Metodologia
1. **Identificar o vicio (1.022):** I obscuridade/contradicao; II omissao (inclusive omissao sobre tese de repetitivo/IAC ou os vicios de fundamentacao do **489 §1** — ex.: acordao que nao enfrenta o Tema 1.113 invocado); III erro material. Apontar o vicio com precisao cirurgica — ED **nao serve para rediscutir o merito**.
2. **Prazo:** **5 dias uteis** (1.023), peticao ao proprio juizo/relator, **sem preparo**.
3. **Efeito (1.026):** ED **interrompem** o prazo do recurso principal — recontar o prazo do zero apos o julgamento (nao confundir com suspensao). Sem efeito suspensivo automatico (eficacia suspensivel pelo juiz no §1).
4. **Prequestionamento (1.025 + Sumula 98/STJ):** consideram-se prequestionados os elementos suscitados nos ED ainda que rejeitados, se o tribunal superior reconhecer o vicio. **Sumula 98/STJ:** ED com proposito de prequestionar **nao** sao protelatorios — afasta a multa do 1.026 §2. So via `validador-imobiliario`. Este e o passo obrigatorio antes de `recursos-excepcionais` quando a tese imobiliaria nao foi expressamente decidida.
5. **Risco de multa (1.026 §2-4):** ate 2% (protelatorios); reiteracao ate 10% + deposito previo; **vedados novos ED apos 2 ED protelatorios**. Avaliar antes de embargar.
6. **Fungibilidade (1.024 §3):** em tribunal, ED podem ser recebidos como agravo interno mediante intimacao previa — atentar.
7. Redigir: enderecamento ao prolator + identificacao do vicio (transcrever o trecho omisso/contraditorio) + pedido de saneamento + (se for o caso) pedido expresso de prequestionamento indicando o dispositivo/tese a ser enfrentado.

## Entrega obrigatoria final
- ED redigidos com o vicio apontado item a item + pedido de saneamento/prequestionamento (com indicacao da tese imobiliaria a prequestionar).
- Parecer de tempestividade (5 dias uteis) + alerta sobre efeito interruptivo e risco de multa protelatoria.

## Guard
Nenhum dispositivo/sumula entra sem `validador-imobiliario` (Sumula 98 via validador); ancoras em `jurisprudencia-imobiliaria`; guard `anti-alucinacao-imobiliaria`. Nao usar ED para rediscutir merito (vira protelatorio). Entrega final pela `suprema-corte-imobiliaria`.
