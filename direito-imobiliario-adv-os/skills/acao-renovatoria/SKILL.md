---
name: acao-renovatoria
description: "Redige acao renovatoria de locacao NAO residencial protegendo o ponto comercial, conferindo os requisitos CUMULATIVOS do art. 51 (contrato escrito e determinado, prazo >=5 anos ou accessio temporis, mesmo ramo ha >=3 anos) e, sobretudo, a DECADENCIA FATAL do §5º (ajuizar no interregno de 1 ano a 6 meses antes do termo), com as excecoes do art. 52 (em shopping o locador nao recusa por uso proprio). Use quando o operador disser: acao renovatoria, renovacao compulsoria do aluguel, proteger o ponto comercial, renovar locacao comercial, prazo pra renovatoria, perdi o prazo da renovatoria."
---

# ACAO RENOVATORIA (arts. 51-52, 71-75, Lei 8.245/91)

> Camada 5 — Locacao. Peca do locatario empresario para renovar compulsoriamente a locacao nao residencial e proteger o fundo de comercio. Anexos: `context/lei-8245-locacao.md`.

## Quando ativa
Locatario comercial quer garantir a renovacao contra a vontade do locador; ou avaliar se ainda ha janela (decadencia) e se os requisitos estao preenchidos.

## Base legal ancorada
- **Art. 51 — requisitos CUMULATIVOS (✅):**
  - **I** — contrato escrito e por prazo determinado;
  - **II** — prazo minimo de **5 anos** (ou soma de contratos escritos ininterruptos = 5 anos — **"accessio temporis"**);
  - **III** — exploracao do **mesmo ramo** por >=3 anos.
  - **§4º** — estende-se a industrias e sociedades civis com fim lucrativo.
- **Art. 51 §5º — DECADENCIA (✅):** a acao deve ser proposta **no interregno de 1 ano (maximo) a 6 meses (minimo) anteriores ao termino** do contrato. 🔴 *Prazo DECADENCIAL fatal — perder a janela mata o direito a renovacao. E a pegadinha nº 1 da renovatoria; conferir a data ANTES de qualquer coisa.*
- **Art. 52 — excecoes (o locador NAO e obrigado a renovar) (✅):** obras do Poder Publico; uso proprio ou transferencia de fundo de comercio de ascendente/descendente.
  - **§2º** — em **shopping center** o locador **NAO pode recusar** com base no inciso II (uso proprio/transferencia).
  - **§3º** — direito a indenizacao por perda do ponto quando a nao renovacao decorrer de proposta melhor de terceiro ou das excecoes.
- **Arts. 71-72 (✅):** requisitos da inicial (prova da exata satisfacao das obrigacoes, indicacao de fiador/garantia, condicoes de renovacao) e da contestacao. **Art. 74 (✅, red. 12.112/09):** nao renovada, o juiz fixa **30 dias** para desocupacao.

## O que produzir (estrutura da inicial)
1. **CHECAR A DECADENCIA PRIMEIRO** (art. 51 §5º): calcular a janela 1 ano-6 meses antes do termo; se fora, alertar o operador — direito extinto (nao ha peca a fazer).
2. Provar os **3 requisitos cumulativos** do art. 51 (contrato escrito determinado; 5 anos ou accessio temporis; 3 anos no mesmo ramo).
3. **Instruir com os requisitos do art. 71:** exata satisfacao das obrigacoes (recibos/quitacoes), indicacao das novas condicoes propostas, indicacao do fiador com anuencia e qualificacao.
4. Pedido: renovacao compulsoria pelo mesmo prazo, fixacao do novo aluguel a mercado; subsidiario, indenizacao por perda do ponto (art. 52 §3º) se a renovacao for negada por causa legitima.
5. Competencia/valor: foro do imovel; valor da causa conforme art. 58 (12 meses do aluguel pretendido).

## Postura honesta
- **Nao ha sumula nem tema repetitivo do STJ especifico sobre renovatoria** — a materia e regida pela **letra da Lei 8.245 + precedentes esparsos**. Nao inventar sumula; ancorar nos arts. 51-52.
- A decadencia do §5º e **fatal e improrrogavel** — nao ha "boa-fe" que a supra. Se o prazo passou, ser honesto: cabe negociar renovacao amigavel, nao acao renovatoria.
- Fora de shopping, o **uso proprio do locador** (art. 52, II) e recusa legitima — a renovatoria nao vence contra ele; cabe indenizacao pelo ponto, nao a renovacao.

## Cross-link soft (nao duplicar)
- Nao renovada e vencido o prazo -> despejo pela `acao-despejo` (art. 59 §1º, VIII para nao residencial).
- Revisao do valor do aluguel fora do contexto renovatorio -> `revisional-de-aluguel`.

## Guard
Nenhum dispositivo sem `validador-imobiliario`; guard `anti-alucinacao-imobiliaria` (decadencia 1 ano-6 meses; sem sumula propria; shopping x art. 52 II). Entrega pela `suprema-corte-imobiliaria` (R1-R4), com R4 conferindo a tempestividade decadencial.
