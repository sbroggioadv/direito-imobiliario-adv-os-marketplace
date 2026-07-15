---
name: base-contratual-imobiliaria
description: "Fundamento de direito material dos contratos imobiliarios do CC/2002 — compra e venda (481-532), despesas de escritura/registro (490), arras/sinal (417-420, redacao NOVA da Lei 14.905/2024), clausulas especiais (retrovenda/preempcao/reserva de dominio/venda ad mensuram) e permuta (533), mais o regime vigente de juros e correcao (SELIC-IPCA, Lei 14.905/2024). Localiza o artigo por grep em context/ e traz texto vigente + requisitos + pegadinhas de reforma. Use quando precisar da base de um contrato de compra e venda, arras, sinal, permuta, ou perguntar quem paga escritura, como calcular juros/correcao, qual a redacao atual do art. 418, esse artigo de contrato mudou."
---

# BASE-CONTRATUAL-IMOBILIARIA — Contratos do CC/2002 aplicados ao imovel

> Camada 1 (Fundacao). Direito material contratual para compromisso, escritura, distrato e pareceres. Nao redige peca: entrega o dispositivo certo, vigente e explicado. Direitos reais (posse/propriedade/hipoteca/promessa-1.417) ficam na `base-direitos-reais-cc`.

## Anexos obrigatorios (context/)
- `context/cc-direitos-reais.md` — CC/2002 (contem tambem os contratos-alvo: compra e venda 481+, arras 417-420, permuta 533, juros/correcao 389/406). **Nunca ler inteiro:** grep do artigo (`grep -n "^Art\. 490" context/cc-direitos-reais.md`) e ler a faixa.
- `context/itbi-e-reformas-tributarias.md` — cruzar o status da **Lei 14.905/2024** (taxa legal) quando o tema for juros/correcao/arras.
- `context/metodologia-imobiliaria.md` — quando chamada pelo `imobiliario-master`.

## Objetivo
Devolver o **texto vigente** + finalidade + requisitos + excecoes de qualquer dispositivo contratual imobiliario, com atencao especial as **reformas de 2024** que o treino pode ter perdido.

## Quando ativar
- Outra skill (compromisso, escritura, distrato, parecer) precisa do fundamento material do contrato.
- O operador pergunta sobre compra e venda, arras/sinal, permuta, clausula especial, quem paga escritura/registro, ou juros/correcao aplicaveis.

## Mapa rapido (tema no grep, numero confirmado no anexo)
- **Compra e venda (481–532)** ✅ — **481** conceito; **482** perfeita com acordo sobre coisa+preco; **490** ✅ **escritura e registro por conta do COMPRADOR** (tradicao por conta do vendedor, salvo pacto); **500** venda *ad mensuram* × *ad corpus* (diferenca > 1/20 → acao *ex empto*/abatimento/resolucao); **502** vicios; **504** direito de preferencia do condomino na venda de fracao ideal.
- **Clausulas especiais** ✅ — retrovenda (**505**), preempcao/preferencia (**513**), reserva de dominio (**521**), venda a contento/sujeita a prova.
- **Permuta (533)** ✅ — aplicam-se as regras da compra e venda.
- **Arras / sinal (417–420)** — ⚠️ **REFORMADO pela Lei 14.905/2024**:
  - **417** ✅ arras confirmatorias: computadas/restituidas na execucao.
  - **418** ⚠️ **NOVA REDACAO (Lei 14.905/2024)**, reestruturada em incisos: **I** — inexecucao por quem **DEU** as arras → a outra parte as retem; **II** — inexecucao por quem **RECEBEU** → quem deu pode haver o contrato por desfeito e **exigir a devolucao mais o equivalente, com atualizacao monetaria, juros e honorarios de advogado** (mencao expressa a *honorarios* = a novidade). 🔴 A redacao antiga (paragrafo unico) e a que muitos modelos "lembram" — usar a de **2024**.
  - **419** indenizacao suplementar (arras = taxa minima). **420** arras **penitenciais** (com arrependimento) = funcao **unicamente indenizatoria**, sem suplementar.
- **Juros e correcao legais** — ⚠️ **Lei 14.905/2024** (efeitos desde **30/08/2024**) alterou **CC 389 e 406**: **juros legais = SELIC deduzido o IPCA**; **correcao monetaria = IPCA** (salvo pactuacao). 🔴 Nao usar o default antigo "1% ao mes (art. 406 c/c 161 §1º CTN)" — esta **desatualizado**. Calculo efetivo → cross-link `calculosjudiciais`.

## Postura honesta / pegadinhas
- 🔴 **Arras art. 418** e **juros/correcao (389/406)** so na redacao **pos-14.905/2024**. Confirmar sempre em `validador-imobiliario` antes de citar.
- **Despesas:** por padrao legal a escritura+registro sao do **comprador** (490) e a tradicao do vendedor — mas isso e **dispositivo, admite pacto em contrario**; ler a clausula concreta antes de afirmar.
- Distrato/retencao (Lei 13.786/2018 + Sumula 543) NAO fica aqui — e a skill `distrato-imobiliario` (C2); esta base so entrega o CC.

## Entrega obrigatoria final
Dispositivo com **texto verbatim** + finalidade + requisitos + excecoes + vigencia (com destaque para 14.905/2024) + ponteiro do trecho lido. Sem confirmacao no anexo, nao entregar redacao.

## Guard
Nada de memoria: grep obrigatorio no anexo. Toda citacao passa por `validador-imobiliario`; toda peca fecha pela `suprema-corte-imobiliaria` (R2 fundamentacao vigente · R3 tributario/calculo correto).
