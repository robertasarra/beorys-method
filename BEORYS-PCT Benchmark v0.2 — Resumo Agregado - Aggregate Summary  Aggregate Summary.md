# BEORYS-PCT v0.2 — Sumário Executivo

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## Identificação

| Campo | Valor |
|---|---|
| Benchmark | BEORYS-PCT v0.2 |
| Data | 2026-06-06 |
| Modelos | 5 |
| Casos | 100 |
| Categorias | 7 |
| Execuções | 2.500 |
| Grupos | A (prosa), B (checklist), C (auto-reflexão), D (executor+LLM-validador), E (BEORYS™) |

---

## Achado principal

O método BEORYS™ (Grupo E — gate externo determinístico fail-closed) apresenta Trigger Activation Rate de **93%**, comparado a 2–23% nos demais grupos. Esta métrica representa o percentual de casos em que o mecanismo de verificação é efetivamente ativado antes da emissão de afirmação.

Os outros grupos apresentam Protocol Compliance Rate comparável em termos absolutos, mas com verificação não ativada na grande maioria dos casos — o que significa que o modelo está "cumprindo o formato" sem verificar de fato.

---

## Métricas de destaque — Grupo E (BEORYS™)

| Métrica | Valor |
|---|---:|
| Trigger Activation Rate | 93% |
| Evidence Attachment Rate | 99% |
| Unauthorized Output Rate | 2% |
| External Gate Block Rate | 6% |
| Recovery Rate | 89% |
| Auditability Score | 0.83 |

---

## Conclusão limitada ao escopo

Dentro do escopo declarado (5 modelos, 100 casos, 7 categorias, 1 run, 2026-06-06), o gate externo determinístico fail-closed do BEORYS™ supera os demais métodos testados em ativação de verificação e auditabilidade, mantendo compliance de protocolo equivalente.

Esta conclusão não é generalização universal. Ver [(BEORYS-PCT Benchmark v0.2 — Limitations.md)]((./BEORYS-PCT Benchmark v0.2 — Limitations.md)).

---

## Documentos relacionados

- [Método (alto nível)]((./BEORYS-PCT Benchmark v0.2 — Method))
- [Tabela completa de resultados]((./BEORYS-PCT Benchmark v0.2 — Results Table))
- [Relatório de validação]((./BEORYS-PCT Benchmark v0.2 — Validation Report))
- [Checklist de evidência]((./BEORYS-PCT Benchmark v0.2 — Evidence Checklist.md))
- [Limitações]((./BEORYS-PCT Benchmark v0.2 — Limitations.md))
- [Reprodutibilidade]((./BEORYS-PCT Benchmark v0.2 — Reproducibility Statement.md))
- [Sumário público narrativo]((./BEORYS-PCT Benchmark v0.2 — Public Summary))

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
