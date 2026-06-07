# Fundamentação acadêmica — BEORYS™

**Tema:** como impor que um modelo de linguagem respeite um protocolo durante a
geração fluente.
**Data da verificação das fontes:** 2026-06-06.

Este documento reúne a literatura que sustenta o método BEORYS™ e a lacuna
estrutural que a obra endereça. Todas as citações abaixo foram **conferidas em
fonte primária** (DOI ou arXiv, HTTP 200 + título conferido) na data acima.
Acompanha a evidência empírica em [`benchmark/`](./benchmark/).

---

## 1. A lacuna

A literatura atual sobre governança e conformidade de modelos de linguagem
converge em uma tese: **a confiabilidade não emerge da fluência do próprio
sistema.** Regras declarativas ("nunca faça X", "verifique antes de afirmar") são
sistematicamente ignoradas conforme a geração avança, e a autoavaliação interna
do modelo não corrige de forma confiável os próprios erros sem um sinal externo
forte.

A lacuna estrutural: as abordagens vigentes tratam a confiabilidade como uma
qualidade a ser **obtida de** um sistema fluente, e não como uma propriedade
**imposta por** uma verificação externa ao sistema verificado. O método BEORYS™
parte exatamente da posição inversa — separar quem gera de quem valida, e fazer da
validação uma trava determinística e de falha-fechada.

---

## 2. Literatura que sustenta o método

Verificada em fonte primária (DOI/arXiv) em 2026-06-06.

| Obra | Identificador | Tipo | Relevância |
|---|---|---|---|
| Zhou et al. — IFEval: Instruction-Following Evaluation for LLMs | arXiv:2311.07911 | arXiv | Instruções verificáveis; a aderência cai conforme o output cresce |
| Madaan et al. — Self-Refine: Iterative Refinement with Self-Feedback | arXiv:2303.17651 | arXiv | Refino iterativo sem fine-tuning |
| Shinn et al. — Reflexion: Language Agents with Verbal Reinforcement Learning | arXiv:2303.11366 | arXiv | Actor–Evaluator–Reflector, sem atualizar pesos |
| Dhuliawala et al. — Chain-of-Verification Reduces Hallucination in LLMs | arXiv:2309.11495 | arXiv | Planejar a verificação ANTES do output final |
| Gou et al. — CRITIC: LLMs Can Self-Correct with Tool-Interactive Critiquing | arXiv:2305.11738 | arXiv | Autocorreção via ferramenta externa (análogo da trava física) |
| Kamoi et al. — When Can LLMs Actually Correct Their Own Mistakes? | TACL 2024 · doi:10.1162/tacl_a_00713 | Revisado por pares | Evidência CONTRA confiar em autocorreção interna sem feedback externo forte |
| Ferraz et al. — DeCRIM: Decompose, Critique and Refine | Findings of EMNLP 2024 · doi:10.18653/v1/2024.findings-emnlp.458 | Revisado por pares | Modelos violam ≥1 restrição em parte significativa das instruções reais |
| Qin et al. — InFoBench: Evaluating Instruction Following (DRFR) | Findings of ACL 2024 · doi:10.18653/v1/2024.findings-acl.772 | Revisado por pares | Decompor em critérios atômicos sim/não |
| Jiang et al. — FollowBench: Multi-level Fine-grained Constraints | ACL 2024 · doi:10.18653/v1/2024.acl-long.257 | Revisado por pares | Restrições finas multi-nível |
| Rebedea et al. — NeMo Guardrails: Programmable Rails | arXiv:2310.10501 (EMNLP 2023) | Revisado por pares | Trilhos externos programáveis |
| Geng et al. — JSONSchemaBench: Structured Outputs Benchmark | arXiv:2501.10868 | arXiv | Decodificação restrita / saída estruturada |
| Suresh et al. — BEAVER: An Efficient Deterministic LLM Verifier | arXiv:2512.05439 | Preprint | On-point com a tese executor ≠ validador |
| Tripathi et al. — The Instruction Gap | arXiv:2601.03269 | Preprint | Aderência inconsistente a instruções custom em ambiente enterprise |
| Song et al. — Evaluating Implicit Regulatory Compliance in LLM Tool Invocation | arXiv:2601.08196 | Preprint | Compliance regulatória implícita em invocação de ferramentas |
| Jin — FASTRIC: Prompt Specification Language for Verifiable LLM Interactions | arXiv:2512.18940 | Preprint | Linguagem de especificação para interações verificáveis |
| Purpura et al. — MOSAIC: Granular Evaluation of LLM Instruction Compliance | arXiv:2601.18554 | Preprint | Avaliação granular/modular de compliance de instrução |

**Regra de uso das fontes:** as âncoras revisadas por pares (IFEval, CoVe, CRITIC,
TACL, DeCRIM, InFoBench, FollowBench, NeMo) sustentam as afirmações centrais; os
preprints recentes (2025–2026) entram **como corroboração**, nunca como base única
de qualquer afirmação forte.

---

## 3. Da literatura à evidência empírica

A literatura **descreve** a lacuna; o **BEORYS Benchmark** a **mede**. Em sua
medição mais recente (**v0.2**), comparando no mesmo conjunto de **100 casos** e
**5 modelos** (**2.500 execuções**) cinco formas de impor o mesmo protocolo — com a
compliance medida sempre na primeira saída e pelo mesmo verificador determinístico:

| Condição | Mecanismo | Compliance (1ª saída) |
|---|---|---:|
| A | Protocolo em prosa | 95% |
| B | Checklist estruturado | 93% |
| C | Autorreflexão | 92% |
| D | Executor + validador-LLM | 93% |
| E | Gate de falha-fechada + trava externa | 95% |

Medida de forma justa e anti-circular, a compliance bruta da primeira saída
converge (~92%–95%) em todos os métodos: a fluência já produz texto que se lê como
conforme. A diferença decisiva está nas demais métricas — o gate externo (E) aciona
a verificação em **93%** dos casos contra **2%** da prosa, produz a menor taxa de
saída não-autorizada (**2%**), não admite a aprovação falsa que o validador-LLM (D)
comete em 2% das saídas inválidas, e atinge a maior auditabilidade (**0,83** contra
**0,60** da prosa). Os resultados observados são consistentes com a tese: a confiabilidade vem
da **autorização externa**, não da fluência.

> O pacote reprodutível público em [`benchmark/`](./benchmark/) corresponde ao run
> **v0.1** (3 métodos · 12 modelos · 576 execuções; prosa 51% → checklist 94% →
> gate 95%). A v0.2 refina a medição: acrescenta verdade-base factual e separa, de
> forma anti-circular, a compliance da primeira saída do bloqueio da trava — o que
> faz a compliance bruta convergir e desloca a diferença para o acionamento do
> gatilho, a saída não-autorizada, a aprovação falsa e a auditabilidade.

---

## 4. Limites da evidência

Para preservar o rigor científico, os limites desta evidência são registrados de
forma explícita:

- o benchmark **descreve um conjunto específico de execuções** (5 modelos, 100
  casos, 2.500 execuções, na data indicada) — **não é prova universal** e não se
  generaliza automaticamente para outros modelos, domínios ou tarefas;
- os resultados **não constituem prova definitiva**; são consistentes com a
  hipótese **nas condições medidas**;
- **novas replicações** — com outros modelos, casos e juízes — podem **fortalecer,
  qualificar ou ajustar** estas conclusões;
- a literatura revisada (§2) **sustenta partes da hipótese**, mas não substitui a
  validação empírica, assim como a validação empírica não dispensa a literatura.

Esta seção não enfraquece a tese central; apenas a enquadra como uma afirmação
**defensável e falsificável**, e não como um absoluto.

---

# Academic foundation — BEORYS™ (English)

**Topic:** how to enforce that a language model respects a protocol during fluent
generation.
**Source verification date:** 2026-06-06.

This document gathers the literature supporting the BEORYS™ method and the
structural gap the work addresses. Every citation below was **verified against its
primary source** (DOI or arXiv, HTTP 200 + title checked) on that date. It
accompanies the empirical evidence in [`benchmark/`](./benchmark/).

## 1. The gap

The current literature on language-model governance and compliance converges on a
single thesis: **reliability does not emerge from the system's own fluency.**
Declarative rules ("never do X", "verify before asserting") are systematically
ignored as generation proceeds, and a model's internal self-assessment does not
reliably correct its own errors without a strong external signal.

The structural gap: prevailing approaches treat reliability as a quality to be
**coaxed out of** a fluent system, rather than as a property **enforced by**
verification external to the system being verified. BEORYS™ takes the inverse
stance — separate the generator from the verifier, and make verification a
deterministic, fail-closed lock.

## 2. Supporting literature

See the verified reference table in the Portuguese section above (§2); each entry
was confirmed against its primary source (DOI/arXiv) on 2026-06-06. Peer-reviewed
anchors support the central claims; recent preprints serve as corroboration only,
never as the sole basis of any strong claim.

## 3. From literature to empirical evidence

The literature **describes** the gap; the **BEORYS Benchmark** **measures** it. In
its most recent run (**v0.2**), across the same set of **100 cases** and **5
models** (**2,500 executions**), comparing five ways of enforcing the same protocol
— with compliance always measured on the first output by the same deterministic
verifier:

| Condition | Mechanism | Compliance (1st output) |
|---|---|---:|
| A | Protocol in prose | 95% |
| B | Structured checklist | 93% |
| C | Self-reflection | 92% |
| D | Executor + LLM validator | 93% |
| E | Fail-closed gate + external lock | 95% |

Measured fairly and anti-circularly, raw first-output compliance converges
(~92%–95%) across all methods: fluency already produces text that reads as
compliant. The decisive difference lies in the other metrics — the external gate
(E) triggers verification in **93%** of cases vs **2%** for prose, yields the lowest
unauthorized-output rate (**2%**), has no false-approval failure mode (which the LLM
validator (D) commits on 2% of invalid outputs), and reaches the highest
auditability (**0.83** vs **0.60** for prose). These observations are consistent with
the thesis: reliability comes from **external authorization**, not from fluency.

> The public reproducible package in [`benchmark/`](./benchmark/) corresponds to the
> **v0.1** run (3 methods · 12 models · 576 runs; prose 51% → checklist 94% → gate
> 95%). v0.2 refines the measurement: it adds factual ground truth and separates,
> anti-circularly, first-output compliance from the lock's blocking — which makes
> raw compliance converge and shifts the difference to trigger activation,
> unauthorized output, false approval, and auditability.

---

## 4. Limits of the evidence

For scientific rigor, the limits of this evidence are stated explicitly:

- the benchmark **describes a specific set of executions** (5 models, 100 cases,
  2,500 runs, on the stated date) — it is **not universal proof** and does not
  automatically generalize to other models, domains, or tasks;
- the results **are not definitive proof**; they are consistent with the hypothesis
  **under the measured conditions**;
- **further replications** — with other models, cases, and judges — may
  **strengthen, qualify, or adjust** these conclusions;
- the reviewed literature (§2) **supports parts of the hypothesis** but does not
  replace empirical validation, just as empirical validation does not dispense with
  the literature.

This section does not weaken the central thesis; it frames it as a **defensible,
falsifiable** claim rather than an absolute.

---

© Roberta Sarra España — BEORYS™. Ver [`LICENSE`](./LICENSE).
