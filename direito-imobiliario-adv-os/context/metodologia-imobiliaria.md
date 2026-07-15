# Anexo — Metodologia do Plugin Direito Imobiliário

> Como o plugin pensa antes de escrever. Pilares de qualidade, fluxo de trabalho (due diligence → peça), correções anti-alucinação travadas e a lista 🟡 proibida. Este anexo governa todas as skills; a `anti-alucinacao-imobiliaria` e a `suprema-corte-imobiliaria` o aplicam a cada fecho de peça.
> Base: design-spec 2026-07-15 + 4 dossiês de pesquisa (fonte oficial capturada 2026-07-15).

---

## 1. Os três pilares

1. **Standalone-first** — recursos processuais, prazos e estrutura de peça são modelados dentro do plugin (espinha do cível). Cross-links com `civel`, `execucao`, `calculosjudiciais`, `tributario-societario`/`holding`, `familia`, `bancario` são **soft** (não duplicar, não depender em runtime). O plugin funciona sozinho.
2. **Anti-alucinação por design** — nenhum dispositivo, súmula, tema ou alíquota entra em peça sem estar ancorado nos anexos `context/`. Jurisprudência com selo ✅ VALIDADA exige `WebFetch` real na fonte oficial no momento do uso (a lista de âncoras é o ponto de partida, não a dispensa). Itens 🟡 nunca viram fato.
3. **Postura honesta nos rachas** — onde a jurisprudência está dividida, o plugin **avisa a divisão**, não promete vitória. Um advogado que sabe do racha protege o cliente; um que esconde vende ilusão. Rachas obrigatórios: Súmula 308 × AF · Tema 796 holdings · retenção 50%→25% (CC 413) · LC 227/2026 × Tema 1.113 · purgação Tema 1.288 pendente.

## 2. Lei VIGENTE 2026 é autoritativa (não o treino)

As reformas de 2022-2026 são o núcleo do diferencial — o treino de jan/2026 pode não tê-las visto ou tê-las visto pela metade. Quando o modelo "lembra" de uma regra antiga, o anexo `context/` **vence**. Reformas-chave:
- **Lei 14.711/2023** (Marco das Garantias — AF reformada + hipoteca extrajudicial). `lei-9514-marco-garantias.md`.
- **Lei 14.382/2022** (SERP — 216-A concordância, 216-B adjudicação extrajudicial). `lrp-6015-serp.md`.
- **Lei 14.905/2024** (taxa legal SELIC-IPCA + arras art. 418). `cc-direitos-reais.md`.
- **LC 214/2025** (IBS/CBS sobre imóveis) + **LC 227/2026** (art. 38 CTN, tensão com o Tema 1.113). `itbi-e-reformas-tributarias.md`.
- **Lei 13.786/2018** (distrato) + **Lei 13.465/2017** (REURB + laje + 216-A concordância).

## 3. O fosso: extrajudicial/registral

Nenhum outro plugin da família cobre cartório/registro. O advogado imobiliário ganha por três competências que a IA genérica não entrega:
1. **Ler matrícula e cadeia dominial** — enxergar o risco escondido (fraude à execução, ônus, indisponibilidade).
2. **Desjudicializar** — resolver no cartório o que ia ao fórum (usucapião 216-A, adjudicação 216-B, retificação 213, dúvida 198-204, REURB).
3. **Montar o negócio certo** — qual instrumento (compromisso × escritura), o que registrar × averbar, quem paga o quê.

Cada fluxo opera **passo a passo** (checklist de documentos + providências + onde protocola + prazo + o que trava), não só cita a lei.

## 4. Fluxo de trabalho — due diligence → peça

**Regra de ouro: DD ANTES da preliminar.** Assinar arras/sinal antes de concluir a due diligence enfraquece a posição negocial. O plugin **sempre** ordena DD → depois preliminar.

### 4.1 O tripé da due diligence (cruzamento — falhar em um compromete o negócio)
| Frente | Pergunta | Onde |
|---|---|---|
| 🏠 O imóvel | Livre de ônus e é o que dizem? | Matrícula atualizada (≤ 30 dias) + IPTU + condomínio |
| 👤 O vendedor | Pode vender e não tem dívida que arraste o bem? | Certidões pessoais/fiscais/trabalhistas (ou societárias) |
| 📄 O contrato | Reflete a matrícula e protege o comprador? | Minuta cruzada com tudo acima |

**Leitura da matrícula:** R = Registro (aquisições, hipoteca, AF); Av = Averbação (construção/habite-se, penhora, indisponibilidade, ações, casamento/divórcio). Concentração dos atos na matrícula = **Lei 13.097/2015 art. 54**. Cadeia dominial: recuar **15-20 anos**. Transmissão só com registro (**CC 1.245**).

**Certidões-chave:** do imóvel (matrícula, ônus reais, ações reais/reipersecutórias, IPTU, condomínio, habite-se; rural: CAR/CCIR/ITR/georreferenciamento SIGEF 🟡); do vendedor PF (distribuidores cíveis/família/execuções fiscais/JF/JT + protestos nas comarcas do domicílio E do imóvel, **PGFN por CPF**, casamento/regime, **CNIB**); do vendedor PJ (contrato social, CND Receita, FGTS, CNDT, recuperação/falência, poderes do signatário, certidões dos sócios); espólio (formal de partilha ou alvará judicial).

**Riscos a mapear:** fraude à execução (Súmula 375 — comum) × fraude à execução FISCAL (art. 185 CTN + Tema 290 — presunção absoluta, matrícula limpa não blinda; puxar PGFN por CPF **e** CNPJ do empresário individual); fraude contra credores (pauliana, CC 158-165); hipoteca construtora × agente financeiro (Súmula 308 — mapear mesmo ineficaz); bem de família; indisponibilidade (CNIB).

**Entregável:** relatório técnico estruturado (imóvel/partes, síntese documental, riscos quantificados + gravidade impeditivo/mitigável/aceitável, cláusulas protetivas, viabilidade). O relatório **é também prova da diligência** (boa-fé objetiva) em litígio futuro.

### 4.2 Escolha do instrumento
- **Compromisso × escritura:** para **eficácia real** (blindar contra terceiros/venda dupla) → **registrar** o compromisso (CC 1.417). Para **adjudicar** (obter a escritura) → não precisa de registro (Súmula 239 STJ + CC 1.418).
- **Escritura pública × instrumento particular:** **CC art. 108** — escritura pública é da **validade** dos atos sobre imóvel de valor > 30 salários mínimos. Exceções (instrumento particular com força de escritura): **AF de imóvel — Lei 9.514/97 art. 38**; **financiamento SFH — Lei 4.380/1964**.

### 4.3 Fecho da peça (Suprema Corte R1-R4)
Toda peça fecha por `suprema-corte-imobiliaria` + `validador-imobiliario`:
- **R1** — fatos/partes/imóvel/matrícula conferem.
- **R2** — fundamentação **vigente** (nunca lei revogada; silêncio=concordância 216-A; arras 14.905; hipoteca extrajudicial; AF reformada 14.711).
- **R3** — tributário correto (ITBI Tema 1.113 + tensão LC 227; imunidade Tema 796 só até o capital; IBS/CBS locação LC 214).
- **R4** — forma/registro/prazo (decadência renovatória 1a-6m, purga 15d, escritura × particular art. 108).

## 5. Correções anti-alucinação TRAVADAS (guard bloqueia o erro)

Erros que a pesquisa pegou e o plugin **nunca** comete:
1. **Tema 1.095 ≠ purgação** — é "AF afasta CDC". Purgação = **Tema 1.288 PENDENTE** + REsp 1.649.595 (racha temporal).
2. **Súmula 619 STJ = bem público** (mera detenção), **não** "usucapião urbano".
3. **Súmula 486 STJ = imóvel locado bem de família**, **não** cota condominial (penhora por cota = **Lei 8.009/90 art. 3º IV**).
4. **"REsp" 1.937.821** (Tema 1.113), **não** "RE".
5. **Arras art. 418 = redação Lei 14.905/2024** (incisos I/II + honorários), não a antiga.
6. **Juros/correção legais = SELIC-IPCA** (14.905/2024), não "1% a.m.".
7. **Hipoteca executa extrajudicialmente** (14.711/2023) — não "só judicial".
8. **Cabe 2ª AF** (sucessiva/superveniente, art. 22 §§3-4) — não "não cabe".
9. **Silêncio do confinante (216-A §2º) = CONCORDÂNCIA** desde a **Lei 13.465/2017** — não "discordância", não "novidade 2026".
10. **Adjudicação compulsória tem via EXTRAJUDICIAL** (216-B, Lei 14.382/2022) — não "sempre judicial".
11. **Garantias da locação são 4** (art. 37 IV, cessão fiduciária de quotas) — não três.
12. **Purga da mora no despejo = 15 dias da citação**, vedada se usada nos **24 meses** — não "prazo da contestação" nem "2x em 12 meses".
13. **Fiador comercial é penhorável** (Tema 1.127 STF + Súmula 549) — não impenhorável.
14. **Renovatória: decadência 1 ano a 6 meses** antes do termo (fatal).
15. **Aluguel entra em IBS/CBS** (LC 214/2025) desde 2026 — não "só IR".
16. **Condomínio edilício = CC 1.331-1.358-A**; incorporação = Lei 4.591 arts. 28+.
17. **Loteamento fechado ≠ condomínio automático** (fechamento vem de lei municipal; taxa a não-associado cai no Tema 492 STF).

## 6. Lista 🟡 PROIBIDA de afirmar sem verificação (guard)

Estes itens **não entram como fato** em peça sem `WebFetch`/confirmação de fonte oficial no momento do uso. Podem ser mencionados como "a confirmar" / "há indícios de", nunca como afirmação categórica:
- **REsp 2.130.141/RS** (racha Súmula 308 × AF) — confirmar inteiro teor.
- **REsp 2.175.618** (redução 50%→25% por CC 413) — confirmar número/teor.
- **REsp 1.910.280** (reafirmação propter rem 2025) — confirmar número/tema.
- **Lei 14.825/2024** (fraude à execução tributária) — confirmar existência/redação.
- **Súmula 194 STJ "versão contemporânea"** (garantia do construtor) — confirmar redação (o CC art. 618 ✅ pode ser citado).
- **Prazo de 15 dias do 216-B** (impugnação do vendedor) — confirmar no CNN vigente.
- **Alíquota RET reduzida** (habitação de interesse social) — confirmar na legislação.
- **RMS 27.358/RJ** (mínimas cautelas / boa-fé) — usar como referência de postura; confirmar antes de citar.
- **Súmula 391 STF** (citação pessoal do confinante) — confirmar (contraponto: CPC 246 §3º).
- **Súmulas 1 e 2 STJ** (despejo — foro/purga) — confirmar.
- **Tema repetitivo de usucapião** ("inexistência de matrícula não impede") — confirmar número.
- **Súmula 637 STJ** (ente público em possessória) — não citar sem verificação.
- **Provimentos CNJ granulares** (149/2023 e emendas 2024-2025: 194/197/202/218/2025) — o Prov. 149/2023 (CNN Foro Extrajudicial) é a base, mas **recebe emendas periódicas** — verificar a versão consolidada no site do CNJ antes de citar dispositivo específico.
- **Valores/critérios da LC 214/2025** (PF contribuinte > 3 imóveis + R$240k/288k; redutor social; regime 3,65% art. 487) — regulamentação infralegal pendente; confirmar antes de aplicar a caso concreto.
- **Lei 14.620/2023** (MCMV/REURB) — confirmar artigo por artigo antes de citar detalhe.

## 7. Fronteiras (o que fica fora)

- **Dentro:** direitos reais, contratos imobiliários, registral/extrajudicial (o fosso), condomínio/incorporação/loteamento/REURB, locação (Lei 8.245), ITBI, possessórias/reais, AF/hipoteca de imóvel, recursos.
- **Fora (cross-link soft):** processual geral → `civel`; execução → `execucao`; ITCMD/holding/integralização (planejamento) → `tributario-societario`/`holding`; partilha → `familia`; veículo (DL 911) → `bancario`; cálculo de distrato/aluguéis/SELIC-IPCA → `calculosjudiciais`. Consumidor puro e sucessões ficam fora.

## 8. Estilo e despersonalização

- Voz técnica, direta, sem enrolação. Peça formatada por `estilo-imobiliario`.
- **Despersonalizado:** autoria "IA Combativa"; o advogado-cliente configura o próprio escritório via `/start-imobiliario`. Zero nome de cliente, zero OAB pessoal, zero dado de escritório específico nas skills e anexos.
