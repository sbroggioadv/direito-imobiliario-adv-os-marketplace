---
name: base-direitos-reais-cc
description: "Recupera e explica dispositivos do Codigo Civil (Lei 10.406/2002) sobre direitos reais imobiliarios sob demanda das outras skills — posse, propriedade, usucapiao, superficie, servidoes, usufruto, promitente comprador, laje e hipoteca. Localiza o artigo por grep em context/cc-direitos-reais.md e traz texto vigente + finalidade + requisitos + excecoes, sem despejar o codigo inteiro nem inventar redacao. Use quando precisar do texto exato de um artigo do CC sobre imovel, ou quando o operador perguntar qual art. rege posse/propriedade/usucapiao/hipoteca/promessa de compra, prazo de usucapiao, base de direito real, esse artigo do CC mudou."
---

# BASE-DIREITOS-REAIS-CC — Recuperador de dispositivos do CC/2002 (Livro III)

> Camada 1 (Fundacao). Fonte de verdade do direito material imobiliario para as demais skills. Nao redige peca: entrega o dispositivo correto, vigente e explicado. Contratos (compra e venda, arras) ficam na `base-contratual-imobiliaria`.

## Anexo obrigatorio (context/)
- `context/cc-direitos-reais.md` — CC/2002, Livro III (arts. 1.196–1.510-E). **Nunca ler inteiro:** localizar o artigo por grep (`grep -n "^Art\. 1.238" context/cc-direitos-reais.md`) e ler so a faixa (do artigo ate o proximo `Art.`).
- `context/metodologia-imobiliaria.md` — quando chamada pelo `imobiliario-master`.

## Objetivo
Devolver, para qualquer artigo/inciso/paragrafo do CC pedido: **texto exato vigente** + **finalidade** + **requisitos** + **excecoes** + **vigencia** — verbatim, sem parafrasear a lei e sem preencher de memoria.

## Quando ativar
- Outra skill (compromisso, usucapiao, possessoria, fiduciaria, parecer, recurso) precisa do fundamento de direito material real.
- O operador pergunta qual artigo rege posse/propriedade/usucapiao/superficie/servidao/usufruto/promessa/laje/hipoteca, ou o prazo de usucapiao.
- Ha duvida sobre a redacao vigente de um dispositivo de direito real.

## Mapa rapido (use o tema no grep, confirme o numero no anexo)
- **Rol dos direitos reais** — art. **1.225** (laje = inciso XIII, incluida pela Lei 13.465/2017). ✅
- **Posse (1.196–1.224)** — 1.196 (teoria objetiva); 1.197 (direta×indireta); 1.198 (detencao ≠ posse); **1.210** tutela possessoria + §1º desforco imediato + §2º **exceptio proprietatis vedada** ("nao obsta a alegacao de propriedade"). ✅
- **Propriedade (1.228–1.276)** — 1.228 (usar/gozar/dispor/reaver; §1º funcao social; §4º-§5º desapropriacao judicial privada). **Aquisicao so pelo registro** — arts. **1.245–1.247** (quem nao registra nao e dono enquanto nao registrado; 1.247 retificacao/anulacao). ✅
- **Usucapiao (1.238–1.244)** ✅ — decorar prazos:
  - **1.238** extraordinaria: **15 anos** (sem titulo/boa-fe); **10 anos** com moradia ou obras produtivas.
  - **1.239** especial rural (*pro labore*): **5 anos**, ate 50 ha, moradia+produtividade, nao ser proprietario de outro.
  - **1.240** especial urbana: **5 anos**, ate 250 m², moradia, nao ser proprietario de outro.
  - **1.240-A** familiar/abandono de lar: **2 anos**, urbano ate 250 m² dividido com ex-conjuge/companheiro que abandonou, moradia, nao ter outro (§ unico: uma so vez).
  - **1.242** ordinaria: **10 anos** (justo titulo + boa-fe); **5 anos** (aquisicao onerosa com registro cancelado + moradia/investimentos).
- **Superficie (1.369–1.377)** — construir/plantar em terreno alheio, escritura publica **registrada**; superficiario arca com encargos/tributos (1.371). Urbana tambem no Estatuto da Cidade (Lei 10.257/2001, arts. 21-24, prazo pode ser indeterminado). ✅
- **Servidoes (1.378–1.389)** · **Usufruto (1.390–1.411)** · **Uso (1.412-1.413)** · **Habitacao (1.414-1.416)** ✅.
- **Promitente comprador (1.417–1.418)** ⭐ — **1.417**: promessa **sem clausula de arrependimento**, por instrumento publico ou particular, **registrada** no RI → **direito real a aquisicao**. **1.418**: pode exigir a escritura definitiva e, na recusa, **requerer ao juiz a adjudicacao** (adjudicacao compulsoria judicial; a extrajudicial e o art. 216-B da LRP → `registros-publicos-serp`/C3). Mitigacao: **Sumula 239 STJ** — adjudicacao **nao se condiciona ao registro** do compromisso (validar em `jurisprudencia-imobiliaria`). ✅
- **Laje (1.510-A a 1.510-E)** ✅ (Lei 13.465/2017) — unidade autonoma com **matricula propria**, sem fracao ideal de terreno; direito de preferencia base×laje (1.510-D).
- **Hipoteca (1.473–1.505)** — objeto no **1.473**; **1.475** ✅ **e NULA a clausula que proibe alienar** o imovel hipotecado (permitido pactuar vencimento antecipado); 1.476 hipotecas sucessivas (2º grau); 1.478-1.479 remicao.

## Pegadinhas / anti-alucinacao (nao repetir erro de treino)
- 🔴 **Hipoteca NAO e mais "so judicial".** O Marco Legal das Garantias (**Lei 14.711/2023**) criou a **execucao EXTRAJUDICIAL da hipoteca no RI** → detalhe na skill `hipoteca-e-execucao-extrajudicial` (C3). Nunca afirmar "hipoteca so executa em juizo".
- 🔴 **Laje** foi incluida em **2017** (Lei 13.465) — nao tratar como novidade recente nem omitir do rol (1.225 XIII).
- Promessa registrada = direito real (1.417); a adjudicacao pode ser **judicial** (1.418) **ou extrajudicial** (216-B LRP) — nao dizer que so cabe a via judicial.

## Entrega obrigatoria final
Citacao do dispositivo (artigo/§/inciso) com **texto verbatim** + finalidade + requisitos + excecoes + confirmacao de vigencia + ponteiro do trecho lido. Duvida de redacao/numero → sinalizar e mandar checar, nunca preencher de memoria.

## Guard
Nenhum dispositivo entregue sem confirmar a redacao no anexo via grep. Na duvida de vigencia/numero, acionar `validador-imobiliario` e bloquear. Toda peca que use isto fecha pela `suprema-corte-imobiliaria`.
