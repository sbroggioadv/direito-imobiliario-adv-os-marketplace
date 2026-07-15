# Anexo — CPC/2015 processual imobiliário (vigente 2026)

> Espinha processual do plugin. Aterra os artigos do CPC (Lei 13.105/2015) e do CC (Lei 10.406/2002) que as camadas 1/4/5/6/7/8 citam mas que não tinham anexo próprio — para que a `base-processual-imobiliaria` e as skills de peça parem de mandar "confirmar art. na fonte" e passem a ancorar aqui.
> Base: texto capturado do Planalto (CPC L13105 e CC L10406compilada) em 2026-07-15 + Súmula 84 conferida na fonte oficial STJ.
> Legenda: ✅ conferido verbatim em fonte oficial · 🟡 não confirmei (não citar em peça sem checar) · 🔴 pegadinha / redação antiga a evitar.

---

## 1. Competência — foro da situação da coisa

- **Art. 47** ✅ — "Para as ações fundadas em **direito real sobre imóveis** é competente o **foro de situação da coisa**."
  - **§1º** ✅ — o autor pode optar pelo foro de domicílio do réu ou de eleição **se o litígio não recair** sobre **propriedade, vizinhança, servidão, divisão e demarcação de terras e nunciação de obra nova** (nesses, o foro é obrigatório).
  - **§2º** ✅ — a **ação possessória imobiliária** será proposta no foro de situação da coisa, "cujo juízo tem **competência absoluta**".
- 🔴 Ação **pessoal** derivada do imóvel (ex.: cobrança de aluguel, cobrança de cotas) admite foro comum/eleição — não confundir com a real. Ajuizar ação real no foro errado = **incompetência absoluta** (não preclui, pode ser declarada de ofício).

## 2. Petição inicial e valor da causa

- **Art. 319** ✅ — requisitos da inicial: I juízo; II qualificação completa das partes (estado civil, união estável, CPF/CNPJ, endereço eletrônico, domicílio); III fato e fundamentos jurídicos; IV pedido com especificações; V **valor da causa**; VI provas; VII opção por audiência de conciliação/mediação. §§1º-3º — a inicial não é indeferida por falta das informações do inc. II quando obtê-las for impossível/excessivamente oneroso ou quando ainda for possível citar o réu.
- **Art. 292** ✅ — o valor da causa consta da inicial/reconvenção e será, entre outros: II — na ação sobre existência/validade/cumprimento/**resolução/resilição/rescisão** de ato jurídico, o valor do ato ou de sua parte controvertida; **IV — na ação de divisão, demarcação e reivindicação, o valor de avaliação da área/bem** objeto do pedido.
  - **§3º** ✅ — o juiz **corrige de ofício e por arbitramento** o valor da causa quando não corresponder ao conteúdo patrimonial em discussão ou ao proveito econômico, recolhendo-se as custas correspondentes.
- 🔴 Valor da causa subdimensionado em ação imobiliária (ex.: usar o venal em vez do de mercado) → impugnação (art. 293) + correção de ofício + custas. Ancore o valor no proveito econômico real.

## 3. Citação dos confrontantes na usucapião

- **Art. 246, §3º** ✅ — "Na ação de **usucapião de imóvel**, os **confinantes serão citados pessoalmente**, **exceto** quando tiver por objeto **unidade autônoma de prédio em condomínio**, caso em que tal citação **é dispensada**."
- Uso: petição de usucapião judicial descreve os confinantes e requer citação pessoal — salvo apartamento/sala em condomínio edilício, em que a confinância se resolve pela própria convenção (dispensa legal).

## 4. Tutela provisória (urgência × evidência)

- **Art. 300** ✅ — **tutela de urgência**: concedida quando houver **probabilidade do direito** (fumus) **e** **perigo de dano ou risco ao resultado útil** (periculum). §1º pode exigir caução (dispensável ao hipossuficiente); §2º liminar ou após justificação prévia; **§3º — não se concede a antecipada quando houver perigo de irreversibilidade** dos efeitos.
- **Art. 311** ✅ — **tutela da evidência**, independe de urgência, quando: I abuso do direito de defesa / propósito protelatório; II fato provável **só por documento** + tese em **repetitivo ou súmula vinculante**; III pedido reipersecutório com prova documental do **contrato de depósito**; IV inicial instruída com prova documental suficiente a que o réu não oponha dúvida razoável.
  - **Parágrafo único** ✅ — "Nas hipóteses dos **incisos II e III**, o juiz **poderá decidir liminarmente**." → 🔴 **liminar de evidência só nos incisos II e III** (I e IV exigem contraditório). Erro comum é pedir liminar de evidência no inciso IV.

## 5. Sentença que supre a declaração de vontade (adjudicação → escritura)

- **Art. 501** ✅ — "Na ação que tenha por objeto a **emissão de declaração de vontade**, a sentença que julgar procedente o pedido, uma vez **transitada em julgado**, **produzirá todos os efeitos da declaração não emitida**."
- Base processual da **adjudicação compulsória judicial**: a sentença substitui a outorga da escritura do vendedor renitente; a carta de sentença registra-se no RI. Cross-link soft `adjudicacao-compulsoria-judicial`; via extrajudicial preferencial = art. 216-B LRP.

## 6. Ações possessórias

- **Art. 554** ✅ — **fungibilidade**: propor uma possessória por outra não obsta a proteção correspondente àquela cujos pressupostos estejam provados (reintegração ↔ manutenção ↔ interdito). §§1º-3º — polo passivo com grande número de pessoas: citação pessoal dos encontrados + edital dos demais, intimação do MP e da Defensoria (se hipossuficientes) e ampla publicidade.
- **Art. 558** ✅ — **força nova × força velha**: rito especial (com liminar do art. 562) quando a ação for proposta **dentro de ano e dia** da turbação/esbulho; passado o prazo, o **procedimento é comum**, "não perdendo, contudo, o caráter possessório".
- **Art. 562** ✅ — estando a inicial bem instruída, o juiz **defere sem ouvir o réu** a **liminar** de manutenção/reintegração; senão, designa **audiência de justificação prévia**. Parágrafo único — contra a **Fazenda Pública** não há liminar sem prévia audiência dos representantes judiciais.
- 🔴 Força velha (> ano e dia) não perde a liminar do 562, mas passa a depender da **tutela de urgência geral** (art. 300). Cross-link `base-direitos-reais-cc` (CC 1.210 §1º desforço imediato · §2º *exceptio proprietatis* vedada).

## 7. Ação de demarcação e de divisão (arts. 569–598)

- **Art. 569** ✅ — cabe: I ao **proprietário** a **demarcação** (obrigar o confinante a estremar os prédios, fixar/aviventar limites); II ao **condômino** a **divisão** (obrigar os consortes a estremar quinhões).
- **Art. 574** ✅ — inicial da demarcatória: instruída com os **títulos de propriedade**, designa o imóvel pela situação/denominação, descreve os limites a constituir/aviventar/renovar e **nomeia todos os confinantes** da linha demarcanda.
- **Art. 581** ✅ — a sentença determina o **traçado da linha demarcanda**; parágrafo único — determina a **restituição da área invadida**, declarando domínio/posse do prejudicado.
- **Art. 588** ✅ — inicial da divisória: instruída com os **títulos de domínio**, indica origem da comunhão, situação/limites/características do imóvel e a qualificação de **todos os condôminos**.
- **Art. 598** ✅ — às divisões aplicam-se os arts. 575 a 578 (legitimidade de qualquer condômino, citação dos réus etc.).
- **Art. 571** ✅ — 🔴 demarcação e divisão podem ser feitas **por escritura pública** se todos os interessados forem maiores, capazes e concordes → oferecer a **via extrajudicial** antes de judicializar (diferencial do plugin). Cross-link `demarcatoria-divisoria-e-embargos-terceiro`.

## 8. Embargos de terceiro (+ Súmula 84 STJ)

- **Art. 674** ✅ — quem, **não sendo parte**, sofrer constrição (ou ameaça) sobre bens que **possua** ou sobre os quais tenha **direito incompatível** com o ato pode pedir seu desfazimento por embargos de terceiro. §1º cabe ao proprietário (inclusive fiduciário) ou possuidor; §2º equipara a terceiro o cônjuge/companheiro (meação), o adquirente em fraude à execução declarada, quem sofre constrição por desconsideração de que não participou, e o credor com garantia real não intimado.
- **Art. 675** ✅ — prazo: a qualquer tempo no conhecimento até o trânsito; na execução/cumprimento, **até 5 dias depois** da adjudicação/alienação/arrematação e **sempre antes da assinatura da carta**.
- **Súmula 84 STJ** ✅ (conferida em fonte oficial STJ) — "É admissível a oposição de **embargos de terceiro** fundados em alegação de **posse advinda do compromisso de compra e venda** de imóvel, **ainda que desprovido do registro**." → protege o **promissário comprador** que ainda não registrou contra penhora/constrição sobre o imóvel prometido. (STJ estende a tese ao imóvel adquirido na planta em construção.)

## 9. Títulos executivos extrajudiciais imobiliários (art. 784)

- **Art. 784, VIII** ✅ — "o **crédito, documentalmente comprovado, decorrente de aluguel de imóvel**, bem como de encargos acessórios, tais como **taxas e despesas de condomínio**" → base da **execução de aluguéis e encargos** (não precisa de ação de cobrança prévia). Cross-link `execucao-alugueis-e-encargos`.
- **Art. 784, X** ✅ — "o **crédito referente às contribuições ordinárias ou extraordinárias de condomínio edilício**, previstas na convenção ou aprovadas em assembleia geral, **desde que documentalmente comprovadas**" → **cota condominial é título executivo extrajudicial** (executa direto, obrigação *propter rem*). Cross-link `cobranca-cotas-condominiais`.
- **Art. 784, V** ✅ — contrato garantido por **hipoteca, penhor, anticrese ou outro direito real de garantia** é título executivo (base da execução de garantia real; o Marco 14.711/2023 abriu ainda a via **extrajudicial** da hipoteca no RI — ver `lei-9514-marco-garantias`).
- 🔴 Sem prova documental do crédito (contrato de locação, convenção/ata de assembleia), o inciso VIII/X **não** confere executividade — ajuizar conhecimento/monitória (art. 785).

## 10. Recursos

- **Art. 1.009** ✅ — da **sentença** cabe **apelação**; §1º questões interlocutórias não agraváveis não precluem e vão em preliminar de apelação/contrarrazões.
- **Art. 1.010** ✅ — a apelação, dirigida ao **juízo de 1º grau**, contém qualificação, exposição de fato/direito, razões de reforma/nulidade e pedido de nova decisão; §§1º-3º — contrarrazões em **15 dias** e remessa ao tribunal **independente de juízo de admissibilidade** na origem.
- **Art. 1.013** ✅ — **efeito devolutivo**: a apelação devolve ao tribunal a matéria impugnada (*tantum devolutum quantum appellatum*); §§1º-2º profundidade da devolução.
- **Art. 1.015** ✅ — **agravo de instrumento** contra interlocutórias **taxativas**: I tutelas provisórias; II mérito do processo; III rejeição de convenção de arbitragem; IV incidente de desconsideração; V gratuidade; VI exibição de documento/coisa; VII exclusão de litisconsorte etc. (rol interpretado com taxatividade mitigada — Tema 988 STJ; confirmar em `jurisprudencia-imobiliaria`).
- **Art. 1.021** ✅ — **agravo interno** contra decisão **monocrática do relator**, ao órgão colegiado; §1º impugnação específica dos fundamentos; §2º contrarraz. em 15 dias e possibilidade de retratação.
- **Art. 1.022** ✅ — **embargos de declaração** contra qualquer decisão para: I esclarecer obscuridade/eliminar contradição; II suprir omissão; III corrigir erro material.
- **Art. 1.023** ✅ — ED opostos em **5 dias**, em petição com indicação do vício, **sem preparo**.
- **Art. 1.029** ✅ — **RE e REsp** (hipóteses da CF) interpostos perante o **presidente/vice do tribunal recorrido**, em petições distintas com exposição de fato/direito, demonstração de cabimento e razões do pedido de reforma.
- **Art. 1.042** ✅ (redação Lei 13.256/2016) — cabe **agravo** contra decisão do presidente/vice que **inadmitir RE ou REsp**, **salvo** quando fundada em **repercussão geral** ou **recursos repetitivos** (nesse caso, agravo interno).
- 🔴 Prazos recursais em **dias úteis** (art. 219); regra geral **15 dias**, **ED = 5 dias**. Confirmar tempestividade (feriado local, suspensão) no caso concreto — cross-link `apelacao-imobiliaria`, `agravo-de-instrumento`, `recursos-excepcionais`, `agravos-excepcionais`, `embargos-de-declaracao`.

## 11. Substrato do CC — vizinhança e outorga conjugal (aterra as peças reais)

- **CC art. 1.277** ✅ — o proprietário/possuidor pode **fazer cessar interferências prejudiciais** à segurança, sossego e saúde provocadas pelo prédio vizinho (**uso anormal da propriedade**). Parágrafo único — pondera natureza do uso, localização e normas de distribuição.
- **CC art. 1.280** ✅ — direito de exigir do vizinho a **demolição ou reparação** do prédio que **ameace ruína**, bem como **caução pelo dano iminente** (**dano infecto**) → base material da **nunciação/demolitória**. Cross-link `nunciacao-demolitoria`.
- **CC art. 1.299** ✅ — **direito de construir**: o proprietário pode levantar as construções que lhe aprouver, **salvo o direito dos vizinhos** e os regulamentos administrativos.
- **CC art. 1.647** ✅ — **outorga conjugal**: ressalvado o art. 1.648, nenhum cônjuge pode, **sem autorização do outro** (exceto na **separação absoluta**): I **alienar ou gravar de ônus real bens imóveis**; II litigar sobre esses bens; III prestar fiança/aval; IV doar bens comuns. → 🔴 **venda de imóvel sem outorga do cônjuge é anulável** (art. 1.649, prazo de 2 anos após o fim da sociedade conjugal); a **outorga uxória/marital** é requisito de validade a checar na due diligence e na escritura. Cross-link `due-diligence-imobiliaria`, `escritura-e-instrumento`.

---

## Guard

Todo dispositivo acima está marcado ✅ (conferido verbatim no Planalto/STJ em 2026-07-15). Citação de artigo **não** listado aqui continua **candidata a verificação** pela `validador-imobiliario` / `anti-alucinacao-imobiliaria` antes de entrar em peça. Nenhum item deste anexo dispensa o fecho pela `suprema-corte-imobiliaria` (R1 competência/foro · R4 forma/prazo/valor da causa).
