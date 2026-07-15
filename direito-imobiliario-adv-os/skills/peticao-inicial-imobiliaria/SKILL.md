---
name: peticao-inicial-imobiliaria
description: Matriz para montar a petição inicial de qualquer ação imobiliária — competência (foro do imóvel), valor da causa, qualificação e requisitos do CPC 319. Use quando o advogado for protocolar uma ação imobiliária e precisar da estrutura da inicial, perguntar "como faço a petição inicial de imóvel", "qual o foro competente", "como calcular o valor da causa imobiliária", "quais documentos anexo", "preciso da outorga do cônjuge?", ou antes de partir para a peça específica (possessória, reivindicatória, usucapião, adjudicação, demarcatória/divisória, embargos de terceiro).
---

# peticao-inicial-imobiliaria — matriz da inicial

É o **andaime**. Chame antes/junto de qualquer skill de peça judicial da Camada 6: aqui você fixa **competência, valor da causa, qualificação, requisitos formais e documentos**; a skill específica preenche a **causa de pedir** e os **pedidos**.

## 1. Base legal ancorada
- **Requisitos da inicial — CPC art. 319** (✅). Petição apta = endereçamento, qualificação das partes, fatos + fundamentos jurídicos, pedido certo e determinado, valor da causa, provas, requerimento de citação. Documentos indispensáveis à propositura (matrícula atualizada + prova do direito).
- **Competência — foro de situação do imóvel** (*forum rei sitae*) para ações fundadas em **direito real imobiliário**; é competência **ABSOLUTA** (não se prorroga, não se afasta por foro de eleição). O artigo exato (CPC art. 47) e o rol de valor da causa vivem em `base-processual-imobiliaria` — **`validador-imobiliario` sela o número antes de fechar**.
- **Valor da causa** = proveito econômico pretendido (em regra, o valor do imóvel ou do benefício da ação). Critério exato no `base-processual-imobiliaria`.

## 2. Estrutura da inicial (checklist)
1. **Endereçamento** — juízo do **foro do imóvel**.
2. **Qualificação** completa das partes + **estado civil e regime de bens** (decisivo: ação real exige consentimento/litisconsórcio do cônjuge — ver §4).
3. **Fatos** (narrativa) → **fundamentos jurídicos** (delegados à skill da ação).
4. **Pedido** certo e determinado (+ tutela de urgência quando couber).
5. **Valor da causa**.
6. **Provas** e **requerimento de citação**.
7. **Documentos**: matrícula atualizada (≤ 30 dias), contrato/título, comprovante de ITBI (se transmissão), procuração, prova específica da ação.

## 3. Matriz por tipo de ação (roteia para a skill certa)

| Ação | Competência | Valor da causa | Documento-chave | Skill |
|------|-------------|----------------|-----------------|-------|
| Possessória (reintegração/manutenção/interdito) | Foro do imóvel | Valor do imóvel ou proveito | Prova da posse + data da agressão | `acoes-possessorias` |
| Usucapião | Foro do imóvel | Valor do imóvel | Planta + memorial (ART/RRT), rol de confrontantes | `usucapiao-judicial` |
| Reivindicatória / imissão | Foro do imóvel | Valor do imóvel | Título registrado (matrícula) | `reivindicatoria-e-imissao-na-posse` |
| Adjudicação compulsória | Foro do imóvel | Valor do imóvel | Promessa + prova de quitação | `adjudicacao-compulsoria-judicial` |
| Demarcatória / divisória | Foro do imóvel | Valor do imóvel/quinhão | Títulos + planta | `demarcatoria-divisoria-e-embargos-terceiro` |
| Embargos de terceiro | Juízo da **constrição** | Valor do bem constrito | Prova da posse/domínio + auto de penhora | `demarcatoria-divisoria-e-embargos-terceiro` |

## 4. Postura honesta
- **Ação real → litisconsórcio/consentimento do cônjuge** (salvo separação absoluta). Sem a outorga/participação, há risco de nulidade. A regra exata (CPC) fica em `base-processual-imobiliaria` — validador confirma.
- **Competência do foro do imóvel é ABSOLUTA** nas ações reais — protocolar em foro errado gera declínio de ofício. (Exceção: embargos de terceiro vão ao **juízo da constrição**, não ao foro do imóvel.)
- **Extrajudicial primeiro**, quando couber: promessa quitada + vendedor recusa → `adjudicacao-compulsoria-extrajudicial` (216-B); posse mansa → `usucapiao-extrajudicial` (216-A). Mais rápido e mais barato — só judicializa se travar.

## 5. Cross-link soft
`civel` (teoria geral da inicial/processo) · `base-processual-imobiliaria` (CPC filtrado: foro, valor da causa, prazos) · `execucao` (cumprimento/execução do julgado).

## 6. Fechamento
Toda peça montada sobre esta matriz fecha por **`suprema-corte-imobiliaria`** (R1 partes/imóvel/matrícula · R4 foro/valor/forma) + **`validador-imobiliario`**.
