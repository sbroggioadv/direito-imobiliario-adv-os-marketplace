---
name: registros-publicos-serp
description: "Fundamento registral do plugin — Lei 6.015/1973 (LRP) com a reforma do SERP (Lei 14.382/2022): principios registrais (prioridade/prenotacao, especialidade, continuidade, legalidade, fe publica, disponibilidade, instancia), atos e prazos eletronicos, e a concentracao de atos na matricula (Lei 13.097/2015 art. 54). Localiza o dispositivo por grep em context/lrp-6015-serp.md e explica alcance + excecoes. Use quando precisar da base registral, ou perguntar como funciona a prenotacao/prioridade, principio da continuidade, o que vale contra terceiro na matricula, concentracao de atos, o que o SERP mudou, se um onus precisa estar averbado."
---

# REGISTROS-PUBLICOS-SERP — Base registral (LRP 6.015/73 + SERP 14.382/22)

> Camada 1 (Fundacao). Espinha do cartorario. Entrega os principios e o regime registral vigente; os procedimentos especificos vivem nas skills C3 (usucapiao-extrajudicial 216-A, adjudicacao-compulsoria-extrajudicial 216-B, retificacao-de-registro 213, duvida-registral 198-204).

## Anexo obrigatorio (context/)
- `context/lrp-6015-serp.md` — Lei 6.015/73 consolidada (reforma 14.382/2022) + Lei 13.097/2015 art. 54. **Nunca ler inteiro:** grep do artigo/tema e ler a faixa.
- `context/metodologia-imobiliaria.md` — quando chamada pelo `imobiliario-master`.

## Objetivo
Dar a **base registral vigente**: o que cada principio garante, o que o SERP digitalizou, e — regra pratica nº 1 — **o que precisa estar na matricula para valer contra terceiro**.

## Quando ativar
- Outra skill precisa do fundamento registral (prioridade, continuidade, qualificacao, concentracao).
- O operador pergunta sobre prenotacao/prazo de validade, principio registral, oponibilidade a terceiro, concentracao de atos na matricula, ou o que o SERP alterou.

## Principios registrais (base do plugin) ✅
- **Prioridade / prenotacao** — art. 186 e 205 (prazo de validade da prenotacao; quem prenota primeiro tem prioridade).
- **Especialidade** (objetiva e subjetiva) — descricao precisa do imovel e das partes.
- **Continuidade** — arts. 195 e 237 (cadeia dominial ininterrupta; so registra quem consta como titular anterior).
- **Legalidade / qualificacao** — o oficial examina o titulo; exigencia indicada de uma so vez, clara e articulada (art. 198, red. 14.382/2022).
- **Presuncao / fe publica**, **disponibilidade**, **instancia** (o registro nao age de oficio, salvo casos legais).
- **So o registro transfere** a propriedade entre vivos (CC 1.245) — cross-link `base-direitos-reais-cc`.

## SERP — Lei 14.382/2022 (o que mudou) ✅
- Institui o **Sistema Eletronico dos Registros Publicos** (converteu a MP 1.085/2021): atos, comunicacoes e certidoes **eletronicos**, interconexao entre serventias.
- Deu vida pratica ao **cartorario extrajudicial** — abriu/aperfeicoou a **usucapiao extrajudicial (216-A)** e criou a **adjudicacao compulsoria extrajudicial (216-B)**. Detalhe procedimental e prazo → skills C3 + `validador-imobiliario` (o **prazo de 15 dias do 216-B** e item ainda a confirmar; nao afirmar como fato).
- **Art. 198** (red. 14.382/2022): a exigencia registral e feita **por escrito, de uma so vez, articuladamente, com data/identificacao/assinatura**.

## Concentracao de atos na matricula — Lei 13.097/2015, art. 54 ⭐ ✅
- **Regra:** todos os onus, gravames, acoes e restricoes que recaem sobre o imovel devem constar da **matricula**; **o que nao esta averbado/registrado nao e oponivel ao terceiro de boa-fe** que adquire confiando na matricula. E o pilar da seguranca juridica registral e da due diligence (cross-link `due-diligence-imobiliaria`, `leitura-matricula-cadeia-dominial`).
- 🔴 **Postura honesta — excecao fiscal:** a concentracao **NAO blinda** contra **fraude a execucao FISCAL**. Alienacao apos a **inscricao em divida ativa** presume-se fraudulenta por **art. 185 do CTN (LC 118/2005) + Tema 290 STJ** (presuncao absoluta; a Sumula 375 STJ nao se aplica a execucao fiscal). Ha decisao de 2ª Turma nesse sentido (REsp 2.173.311/PE), mas o que vincula por tras e o **Tema 290** — nunca dizer que o STJ criou "presuncao nova". Consequencia pratica: matricula limpa **nao** dispensa puxar CND/PGFN por **CPF e CNPJ** do vendedor (sobretudo empresario individual). O conflito art. 54 Lei 13.097 × art. 185 CTN **nao foi resolvido** pelo STJ.

## Entrega obrigatoria final
Principio/dispositivo com alcance + excecoes + ponteiro do trecho do anexo. Ao tocar procedimento de 216-A/216-B/213/198-204, remeter a skill C3 correspondente e nao inventar prazo/etapa.

## Guard
Grep obrigatorio no anexo; nada de memoria. Prazo do 216-B e detalhes procedimentais → confirmar em `validador-imobiliario` antes de citar. Peca fecha pela `suprema-corte-imobiliaria` (R4 forma/registro/prazo).
