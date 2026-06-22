# BEORYS-PCT v0.2 — Significância estatística e intervalos de confiança
> Preenche a limitação #4 ("absent statistical significance"). Calculado sobre os resultados agregados do run v0.2 (n = **500 execuções por grupo**; 100 casos × 5 modelos). Não expõe dataset, prompts nem critérios de bloqueio (segredo industrial preservado).
> Método: proporção por grupo, **IC 95% por escore de Wilson**; comparação entre grupos por **teste z de duas proporções (pooled)**, p bilateral.

## 1. Trigger Activation Rate — o diferencial central
| Grupo | Taxa | IC 95% (Wilson) |
|---|---:|---|
| A — Prosa | 2% | [1.1%, 3.6%] |
| B — Checklist | 23% | [19.5%, 26.9%] |
| C — Autorreflexão | 23% | [19.5%, 26.9%] |
| D — Executor + validador-LLM | 2% | [1.1%, 3.6%] |
| **E — BEORYS™** | **93%** | **[90.4%, 94.9%]** |

**E vs B (melhor baseline):** z = 22.4 · **p ≈ 2.3 × 10⁻¹¹¹**. Os ICs de E e de qualquer baseline **não se sobrepõem** → diferença estatisticamente robusta, não ruído.

## 2. Protocol Compliance Rate — honestidade: aqui NÃO há diferença
| Grupo | Taxa | IC 95% |
|---|---:|---|
| A — Prosa | 95% | [92.7%, 96.6%] |
| E — BEORYS™ | 95% | [92.7%, 96.6%] |

**E vs A:** z = 0.00 · **p = 1.00** → **empate**. A conformidade *bruta* é comparável entre grupos. **O valor do BEORYS™ não está em "cumprir mais", e sim em (1) garantir que a verificação dispare (§1), (2) não ser passível de aprovação falsa (§4) e (3) ser auditável (§5).** Declarar isto explicitamente é mais forte e mais defensável que destacar só "93% vs 2%".

## 3. Unauthorized Output Rate (menor = melhor)
| Grupo | Taxa | IC 95% |
|---|---:|---|
| E — BEORYS™ | 2% | [1.1%, 3.6%] |
| B — Checklist | 6% | [4.2%, 8.4%] |

**E vs B:** z = −3.23 · **p = 0.001** → redução significativa de saídas não-autorizadas.

## 4. False Pass Rate — modo de falha que só os baselines têm
- **D (executor + validador-LLM):** 2% [1.1%, 3.6%] das saídas inválidas foram **aprovadas** pelo validador-LLM.
- **E (BEORYS™):** **0% por design** — a trava determinística *fail-closed* não tem o modo de falha "aprovar o inválido".

## 5. Auditability Score
E = 0.83 vs 0.60–0.66 dos baselines (escore 0–1; rubrica de alto nível — fórmula operacional protegida).

---

### Leitura de uma linha
Compliance bruta empata (p=1.00); o que diferencia o BEORYS™ — com significância estatística — é **onde a verificação dispara** (p≈10⁻¹¹¹), **não aprovar o inválido** (0% vs 2%) e **reduzir saída não-autorizada** (p=0.001).

*Limitações que permanecem: execução única (2026-06-06, reps=1) → sem estabilidade temporal; resultados válidos no escopo testado (5 modelos, 100 casos, 7 categorias). Ver `BEORYS_PCT_v0.2_LIMITATIONS.md`.*
