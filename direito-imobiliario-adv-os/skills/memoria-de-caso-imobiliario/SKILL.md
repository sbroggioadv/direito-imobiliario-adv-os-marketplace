---
name: memoria-de-caso-imobiliario
description: Mantém o estado vivo do caso imobiliário — imóvel, matrícula, partes, contrato, fase, registros/averbações, ITBI e prazos — para que as skills não repitam perguntas nem percam contexto. Use quando o advogado disser "guarda os dados do caso", "onde paramos?", "atualiza a matrícula/os dados", "qual o status?", "continua o caso do imóvel X", ao iniciar qualquer trabalho pelo imobiliario-master, ou quando uma skill precisar recuperar/gravar fatos do imóvel. Também guarda o perfil do escritório vindo do onboarding.
---

# memoria-de-caso-imobiliario — estado do caso

Fonte única de verdade do caso durante a sessão. Toda skill **lê antes** (para não repetir pergunta) e **grava depois** (fatos novos, decisões, resultado da revisão). Mantenha um bloco estruturado e legível; atualize-o em vez de recriar.

## Ficha do caso (campos)
**Perfil do escritório** (do `imobiliario-onboarding`): advogado/OAB, cidade/UF, foro habitual, persona (avulso / imobiliária / cartorário), lado predominante, preferências de peça.

**Imóvel**
- Tipo (urbano/rural; casa/apto/lote/gleba/sala), endereço, área.
- **Matrícula nº + cartório de RI** (ou "sem matrícula" / "só transcrição").
- Nº de contribuinte/IPTU; valor venal; valor de mercado declarado.
- Ônus/gravames: hipoteca, alienação fiduciária, penhora, usufruto, servidão, indisponibilidade (CNIB).
- Concentração na matrícula conferida? (Lei 13.097/2015 art. 54).

**Partes**
- Cliente + lado (comprador/vendedor/possuidor/locador/locatário/condômino/credor/fiduciante).
- Contrária(s); confrontantes (usucapião/demarcatória); cônjuges (outorga — CC 1.647); espólio/inventariante; PJ e representante.

**Contrato / negócio**
- Espécie (compromisso, escritura, locação, incorporação, doação, permuta), **data** (crucial p/ distrato: pré/pós Lei 13.786/2018), valor, quitação, cláusulas relevantes (irretratabilidade, arras, tolerância, garantia locatícia).
- Registrado? averbado? (define direito real e título executivo).

**Fase / procedimento**
- Extrajudicial (cartório/RI) · judicial · administrativo (município/ITBI) · recursal.
- Se judicial: nº do processo, vara/foro, rito, o que já ocorreu (liminar, citação, contestação, sentença).
- Se fiduciária: houve notificação de mora? consolidação? leilão (1º/2º)? prazo de purga (15d) em aberto?

**Tributário do imóvel**
- ITBI: pago? valor/base usada; município arbitrou por "valor de referência"? (Tema 1.113 — possível defesa/restituição). Imunidade em integralização? (Tema 796 — só até o capital).
- Distinguir de ITCMD (doação/herança).

**Prazos e alertas**
- Prazos fatais em aberto: renovatória (1 ano-6 meses), revisional (após 3 anos), purga (15d), recurso, prescrição/decadência.
- Rachas que afetam o caso (Súmula 308 × AF; retenção 50% distrato; Tema 796 holding; LC 227 × Tema 1.113).
- Pendências de verificação (âncora 🟡 ainda não confirmada — o guard trava).

**Histórico / decisões**
- Trilha definida pela triagem; skills já acionadas; peças produzidas; resultado da `suprema-corte-imobiliaria` (R1-R4).

## Regras
- **Não invente dados.** Campo desconhecido = "a confirmar", nunca preenchido por suposição.
- Dado sensível fica no estado local do caso; nada de expor terceiros fora do necessário.
- Ao retomar ("onde paramos?"), devolva um resumo curto: imóvel + partes + fase + próximo passo + prazos em aberto.
- Marque cada fato jurídico com a âncora quando houver, para o `validador-imobiliario` cruzar depois.
