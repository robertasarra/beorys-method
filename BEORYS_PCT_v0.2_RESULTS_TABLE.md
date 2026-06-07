# BEORYS-PCT v0.2 — Tabela de Resultados Agregados

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Escopo:** 5 modelos, 100 casos, 7 categorias, 2.500 execuções  
**Titular:** Roberta Sarra España

---

## Tabela principal — métricas por grupo de instrução

| Metric | A (Prose) | B (Checklist) | C (Self-reflection) | D (Executor + LLM-validator) | E (BEORYS™) |
|---|---:|---:|---:|---:|---:|
| Protocol Compliance Rate | 95% | 93% | 92% | 93% | 95% |
| Trigger Activation Rate | 2% | 23% | 23% | 2% | 93% |
| Factual Assertion Detection Rate | 71% | 72% | 75% | 73% | 71% |
| Evidence Attachment Rate | 95% | 87% | 93% | 94% | 99% |
| Unauthorized Output Rate | 3% | 6% | 5% | 5% | 2% |
| Self-Correction Failure Rate | 0% | 1% | 3% | 0% | 4% |
| External Gate Block Rate | — | — | — | — | 6% |
| False Pass Rate | — | — | — | 2% | — |
| Recovery Rate | — | — | — | — | 89% |
| Auditability Score | 0.60 | 0.64 | 0.66 | 0.61 | 0.83 |

---

## Notas de interpretação

1. **Protocol Compliance Rate** mede conformidade estrutural com o protocolo canônico, não veracidade factual das afirmações.

2. **Trigger Activation Rate** é a métrica que distingue funcionalmente o Grupo E dos demais. Um Trigger Activation Rate de 93% (E) vs. 2–23% (A–D) indica que o gate BEORYS™ ativa a verificação na esmagadora maioria dos casos — enquanto os demais métodos deixam a maior parte das afirmações sem verificação ativada.

3. **External Gate Block Rate (Grupo E — 6%)** representa o volume de outputs rejeitados pelo gate determinístico antes de serem emitidos. Esses bloqueios são a evidência de funcionamento fail-closed: saídas não conformes nunca chegam ao receptor.

4. **Auditability Score** reflete a rastreabilidade e verificabilidade da cadeia decisória, não apenas o resultado final.

5. **Métricas marcadas com —** não se aplicam ao grupo em questão por design do método.

---

## Advertências

- Estes são resultados **agregados** de uma execução (v0.2, 2026-06-06). Não extrapolam automaticamente para outros domínios, conjuntos de tarefas ou modelos.
- Os dados individuais por modelo, por caso e por execução são evidência bruta protegida — ver [BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md](./BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md).
- Para limitações completas, ver [BEORYS_PCT_v0.2_LIMITATIONS.md](./BEORYS_PCT_v0.2_LIMITATIONS.md).

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*  
*Citação autorizada com atribuição: Roberta Sarra España, BEORYS-PCT v0.2, 2026.*
