---
name: base-processual-imobiliaria
description: "Espinha processual STANDALONE do plugin (CPC/2015 filtrado para o imobiliario, sem depender do plugin civel) — competencia pelo foro da situacao do imovel, possessorias (fungibilidade 554, forca nova x velha 558, liminar 562), valor da causa, prazos em dias uteis. Entrega a regra processual aplicavel e manda confirmar no validador antes de citar em peca. Use quando precisar da base processual de uma acao imobiliaria, ou perguntar em que foro se ajuiza acao sobre imovel, cabe liminar na possessoria, forca nova ou velha, qual o valor da causa, prazo do rito."
---

# BASE-PROCESSUAL-IMOBILIARIA — CPC/2015 filtrado (standalone)

> Camada 1 (Fundacao). A espinha do civel **reaproveitada e autossuficiente** — o plugin nao depende do plugin `civel`. Entrega a regra processual aplicavel ao contencioso imobiliario; a peca em si e das camadas C6/C7/C8.

## Anexos (context/)
- `context/jurisprudencia-imobiliaria.md` — ancoras processuais das possessorias/usucapiao (grep do tema).
- `context/metodologia-imobiliaria.md` — quando chamada pelo `imobiliario-master`.
- **Nao ha anexo de CPC integral no plugin.** Por isso: as citacoes de artigo do CPC abaixo sao a **regra aplicavel**, mas **so entram em peca apos confirmacao ao vivo / `validador-imobiliario`** (fetch da fonte oficial). Nunca "colar de memoria" numero de artigo de CPC sem checar.

## Objetivo
Dar a moldura processual da acao imobiliaria: **onde** ajuiza, **qual rito**, **cabe liminar?**, **valor da causa**, **prazos** — de forma standalone.

## Quando ativar
- Skill de peca (possessoria, reivindicatoria, usucapiao judicial, adjudicacao judicial, demarcatoria) precisa da moldura processual.
- O operador pergunta foro/competencia, cabimento de liminar, forca nova×velha, valor da causa ou prazo.

## Competencia — foro da situacao do imovel
- Acoes fundadas em **direito real sobre imoveis** correm no **foro da situacao da coisa** (regra do CPC — confirmar o art. na fonte, tipicamente **art. 47**). Nas acoes de **propriedade, vizinhanca, servidao, divisao/demarcacao, nunciacao de obra nova e posse**, o foro da situacao do imovel e **absoluto** (nao se admite eleicao). Direito **pessoal** derivado do imovel (ex.: cobranca) admite foro comum/eleicao.
- Consequencia: ajuizar no foro errado em acao real = risco de incompetencia absoluta. Confirmar sempre.

## Possessorias (CPC 554 / 558 / 562) ✅ (ancorado em dossie)
- **Art. 554** — **fungibilidade**: reintegracao (esbulho), manutencao (turbacao) e interdito proibitorio (ameaca) sao **intercambiaveis** — pedir uma e obter outra conforme a prova.
- **Art. 558** — **forca nova × forca velha**: esbulho/turbacao ha **menos de ano e dia** → rito especial com **liminar possessoria**; **mais de ano e dia** → rito comum (sem a liminar do 562, mas ainda cabe tutela de urgencia geral).
- **Art. 562** — concessao de **liminar** de manutencao/reintegracao (com ou sem justificacao previa).
- Autotutela: **desforco imediato** do possuidor (CC 1.210 §1º, "contanto que o faca logo") — cross-link `base-direitos-reais-cc`.

## Valor da causa e prazos
- **Valor da causa** — deve refletir o **proveito economico** (ex.: valor do imovel/da posse disputada); confirmar o artigo do CPC (tipicamente **art. 292**) antes de citar. Erro no valor = impugnacao/emenda.
- **Prazos em dias uteis** (CPC 219); regra geral 15 dias; ED 5 dias. Confirmar contagem no caso concreto.

## Postura honesta / pegadinhas
- Como o plugin **nao embarca o CPC integral**, todo numero de artigo processual e **candidato a verificacao** — a skill entrega a regra e o provavel dispositivo, o `validador-imobiliario` confirma. Melhor entregar a regra certa com "confirmar art." do que citar numero errado.
- Nao confundir **possessoria** (protege a posse) com **petitoria/reivindicatoria** (discute a propriedade — CC 1.228): na possessoria vige a **exceptio proprietatis vedada** (CC 1.210 §2º).

## Entrega obrigatoria final
Moldura processual: foro/competencia + rito + cabimento de liminar + valor da causa + prazo, cada citacao de CPC marcada como **confirmar em validador** quando nao ancorada em dossie. As possessorias 554/558/562 estao ancoradas.

## Guard
Numero de CPC nao ancorado nao entra em peca sem checagem ao vivo / `validador-imobiliario`. Peca fecha pela `suprema-corte-imobiliaria` (R1 competencia/foro · R4 forma/prazo/valor da causa).
