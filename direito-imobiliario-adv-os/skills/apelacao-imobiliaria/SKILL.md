---
name: apelacao-imobiliaria
description: "Redige apelacao (CPC 1.009-1.014) contra sentenca em causa imobiliaria — possessoria, usucapiao, adjudicacao, reivindicatoria, condominio, distrato, duvida registral (LRP 202) — no prazo de 15 dias uteis, com preparo sob pena de desercao (1.007), efeito suspensivo como regra (1.012) MAS so efeito DEVOLUTIVO em locacao/despejo (Lei 8.245 art. 58, IV — execucao provisoria), causa madura (1.013 §3) e honorarios recursais (85 §11). Use quando o operador disser apelar, apelacao, recorrer da sentenca, sentenca improcedente, despejo decretado, error in judicando, efeito suspensivo, causa madura, apelar da duvida registral."
---

# APELACAO-IMOBILIARIA — CPC 1.009-1.014

> Camada 8 (recursos). Recurso por excelencia contra a sentenca. **Standalone** — carrega o CPC inline; nao depende do plugin civel. Preparo no ato sob pena de desercao.

## Anexos e skills de apoio
- `context/lei-8245-locacao.md` (art. 58, IV — efeito devolutivo no despejo/locacao) + `context/jurisprudencia-imobiliaria.md` (honorarios recursais 85 §11; ancoras que sobem).
- Base processual em `base-processual-imobiliaria`; ancoras em `jurisprudencia-imobiliaria`; validacao em `validador-imobiliario`.

## Objetivo
Reformar ou anular a sentenca com razoes que ataquem cada capitulo/fundamento, tempestiva, preparada e com o pedido de efeito CORRETO (a pegadinha imobiliaria mora aqui).

## Quando ativar
- Houve **sentenca** (485 terminativa ou 487 definitiva) em acao imobiliaria e a parte quer recorrer.
- Sentenca em **duvida registral** (natureza administrativa) — cabe apelacao (LRP art. 202 ✅).
- Gatilhos: "apelar", "apelacao", "recorrer da sentenca", "improcedente", "despejo decretado", "efeito suspensivo", "causa madura".

## Metodologia
1. **Cabimento (1.009):** da **sentenca**. Interlocutorias **nao agravaveis** nao precluem e vao em **preliminar de apelacao ou contrarrazoes** (§1) — levantar as que cabem (ex.: indeferimento de prova pericial de avaliacao). Cross-link `contrarrazoes-e-contraminuta`.
2. **Tempestividade:** **15 dias uteis** (1.003 §5); dobro por sujeito (Fazenda em REURB/desapropriacao etc.). Conferir feriado local (1.003 §6) — se nao comprovado, tratar como SANAVEL, confirmar via `validador-imobiliario`.
3. **Preparo (1.007):** comprovar **preparo + porte** no ato, **sob pena de desercao**. Insuficiencia -> 5 dias para suprir (§2); ausencia -> recolher em **dobro** (§4). Isentos no §1. Base de calculo = valor da causa (imovel: valor venal/mercado).
4. **Forma (1.010):** peticao de interposicao ao **juizo de 1o grau** + razoes; apelado intimado para contrarrazoes (15 dias). Remessa ao tribunal **independe de admissibilidade na origem** (§3).
5. **Error in procedendo x in judicando:** preliminares de nulidade (procedendo — ex.: ausencia de citacao de confrontante em usucapiao, CPC 246 §3º) + merito recursal (judicando), atacando cada fundamento.
6. **Efeito do recurso — DIVISOR IMOBILIARIO:**
   - **Regra geral (1.012):** apelacao tem **efeito suspensivo**. Excecoes de efeito imediato no §1 (ex.: confirma/concede/revoga tutela provisoria — comum em possessoria/consolidacao fiduciaria).
   - **🔴 LOCACAO/DESPEJO — Lei 8.245 art. 58, IV ✅:** nas acoes da Lei do Inquilinato os recursos sao recebidos **SO no efeito devolutivo** — a sentenca de **despejo executa PROVISORIAMENTE** (execucao provisoria mediante caucao real/fidejussoria de 6 a 12 meses de aluguel — art. 64 no despejo por denuncia). NUNCA prometer que a apelacao "segura" o despejo. Para tentar obstar, requerer **efeito suspensivo ope iudicis ao relator (§4 do 1.012)** com probabilidade de provimento + risco de dano — mas avisar que a regra e a execucao provisoria.
7. **Efeito devolutivo + causa madura (1.013 §3):** o tribunal julga **desde logo o merito** se reformar sentenca 485, decretar nulidade sanavel ou suprir omissao de pedido — requerer expressamente quando favoravel.
8. **Honorarios recursais (85 §11):** o tribunal **majora** os honorarios pelo trabalho em grau recursal (limites §§2-3). So via `validador-imobiliario`.

## Entrega obrigatoria final
- Peticao de interposicao + razoes combatendo cada fundamento (preliminares + merito) + **pedido de efeito correto** (suspensivo como regra; nos casos de locacao/despejo, pedido de efeito suspensivo ope iudicis com a ressalva do art. 58, IV).
- Comprovacao de preparo calculada + parecer de tempestividade + nota sobre causa madura e honorarios recursais.

## Guard
Sumula/tese so via `validador-imobiliario`; ancoras em `jurisprudencia-imobiliaria`; guard `anti-alucinacao-imobiliaria`. **Jamais** afirmar que a apelacao suspende o despejo — art. 58, IV torna o recurso so devolutivo. Preparo ausente/insuficiente = risco de desercao. Entrega final pela `suprema-corte-imobiliaria`.
