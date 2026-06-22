# BEORYS™ — Registro Público de Autoria e Método

**BEORYS™** é o **Plano de Controle para Trabalho com IA** (*AI Work Control Plane*) — uma obra e metodologia proprietária de **Continuidade, Autorização e Prova**, desenvolvida por Roberta Sarra España.

---

## Princípio fundador
> **"A fluência pode redigir; não pode autorizar."**

A tese central: o problema não é ensinar uma regra ao LLM; é **obrigar que a verificação seja executada no momento correto**. A solução é separar **produção** de **autorização** — o LLM gera, mas a autorização vem de verificação externa, determinística, auditável e de **falha-fechada**. *Produzir ≠ autorizar.*

---

## O que é este repositório
Registro público de autoria, prioridade, fundamentação acadêmica, resultados agregados e integridade documental. **Não é** um pacote reprodutível: implementação, prompts, critérios de bloqueio, scripts, dataset integral e lógica de gate permanecem protegidos como segredo industrial (`legal/TRADE_SECRET.md`).

---

## Resultados (BEORYS-PCT v0.2)
Benchmark comparativo entre 5 grupos de instrução (A–E), **5 modelos × 100 casos × 7 categorias = 2.500 execuções** (reps = 1), em 2026-06-06.
Modelos: `gpt-4o-mini`, `claude-haiku-4.5`, `gemini-3.5-flash`, `llama-3.3-70b-instruct`, `deepseek-chat-v3.1` (ver [MODELS](benchmark/BEORYS_PCT_v0.2_MODELS.md)).

### Leia isto primeiro — qual é (e qual não é) a vantagem
A **conformidade bruta** (Protocol Compliance) é **estatisticamente igual** entre os grupos — BEORYS™ 95% × Prosa 95% (p = 1.00). **A vantagem do BEORYS™ não é "cumprir mais"**, e sim:

| Dimensão | BEORYS™ (E) | Baselines | Significância |
|---|---:|---:|---|
| **Trigger Activation** (a verificação dispara) | **93%** | 2–23% | z=22.4 · **p≈2×10⁻¹¹¹** |
| **False Pass** (aprovar o inválido) | **0%** (por design) | 2% (grupo D) | modo de falha ausente em E |
| **Unauthorized Output** (menor=melhor) | **2%** | 6% (B) | p=0.001 |
| **Auditability** (0–1) | **0.83** | 0.60–0.66 | — |

ICs 95% e testes completos: [STATISTICS](benchmark/BEORYS_PCT_v0.2_STATISTICS.md). Tabela bruta: [RESULTS_TABLE](benchmark/BEORYS_PCT_v0.2_RESULTS_TABLE.md).

> Em uma linha: **compliance empata; o que diferencia o BEORYS™ — com significância — é onde a verificação dispara, não aprovar o inválido e ser auditável.**

---

## Documentos públicos

### Autoria e reivindicação
| Documento | Descrição |
|---|---|
| [CLAIM-001.md](claims/CLAIM-001.md) | Declaração pública de autoria e prioridade |

### Metodologia e benchmark
| Documento | Descrição |
|---|---|
| [BEORYS_PCT_v0.2_PUBLIC_SUMMARY.md](benchmark/BEORYS_PCT_v0.2_PUBLIC_SUMMARY.md) | Sumário público do benchmark |
| [BEORYS_PCT_v0.2_AGGREGATE_SUMMARY.md](benchmark/BEORYS_PCT_v0.2_AGGREGATE_SUMMARY.md) | Sumário executivo agregado |
| [BEORYS_PCT_v0.2_METHOD.md](benchmark/BEORYS_PCT_v0.2_METHOD.md) | Declaração do método (alto nível) |
| [BEORYS_PCT_v0.2_RESULTS_TABLE.md](benchmark/BEORYS_PCT_v0.2_RESULTS_TABLE.md) | Tabela de resultados agregados |
| [BEORYS_PCT_v0.2_STATISTICS.md](benchmark/BEORYS_PCT_v0.2_STATISTICS.md) | Significância estatística e intervalos de confiança (IC95 Wilson + testes z) |
| [BEORYS_PCT_v0.2_MODELS.md](benchmark/BEORYS_PCT_v0.2_MODELS.md) | Modelos avaliados (nomes e provedores) |
| [BEORYS_PCT_v0.2_VALIDATION_REPORT.md](benchmark/BEORYS_PCT_v0.2_VALIDATION_REPORT.md) | Relatório de validação pública |
| [BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md](benchmark/BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md) | Checklist de evidência pública vs. protegida |
| [BEORYS_PCT_v0.2_LIMITATIONS.md](benchmark/BEORYS_PCT_v0.2_LIMITATIONS.md) | Limitações declaradas |
| [BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md](benchmark/BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md) | Declaração de reprodutibilidade |

### Fundamentação acadêmica
| Documento | Descrição |
|---|---|
| [FUNDAMENTACAO_ACADEMICA.md](literature/FUNDAMENTACAO_ACADEMICA.md) | Embasamento em literatura revisada |
| [REFERENCES.md](literature/REFERENCES.md) | Lista de referências verificadas |
| [LITERATURE_MAP.md](literature/LITERATURE_MAP.md) | Mapa afirmação → fonte |

### Segredo industrial e licença
| Documento | Descrição |
|---|---|
| [TRADE_SECRET.md](legal/TRADE_SECRET.md) | Fronteira entre público e protegido |
| [NOTICE.md](NOTICE.md) | Todos os direitos reservados |
| [LICENSE.md](LICENSE.md) | Termos de uso do repositório público |

### Integridade documental
| Documento | Descrição |
|---|---|
| [HASH_POLICY.md](integrity/HASH_POLICY.md) | Política de hashes SHA-256 |
| [SHA256_REGISTRY.md](integrity/SHA256_REGISTRY.md) | Registro de hashes dos documentos públicos |
| [RELEASE_INTEGRITY.md](integrity/RELEASE_INTEGRITY.md) | Declaração de integridade desta versão |

---

## O que este repositório não contém

- Código-fonte de gates, validadores, pipeline ou scripts internos
- Prompts internos completos ou variações de prompts
- Dataset integral do benchmark (casos, verdades-base, saídas brutas)
- Critérios proprietários de bloqueio, thresholds ou autorização
- Lógica operacional detalhada dos gates
- Toolkit profissional ou qualquer material de implementação
- Capítulos do livro ou termos comerciais

A ausência desses itens é **deliberada** — ver [TRADE_SECRET.md](legal/TRADE_SECRET.md).

---

## Integridade e verificação
SHA-256 de todos os documentos públicos em `integrity/SHA256_REGISTRY.md`. Hash-mestre privado do run v0.2 em custódia para auditoria independente sob NDA. *(Recomendado: ancorar o hash-mestre em OpenTimestamps para prova pública de data certa — ver roadmap v0.3.)*

## Como citar
```
España, Roberta Sarra. BEORYS™: Plano de Controle para Trabalho com IA.
Registro público de autoria e prioridade. 2026.
https://github.com/robertasarra/beorys-method
```
Formato estruturado: `CITATION.cff`.

---

## Contato

Roberta Sarra España — titular exclusiva de todos os direitos sobre BEORYS™.
Para licenciamento, auditoria ou parceria: conforme [NOTICE.md](NOTICE.md).

---
*Versão pública: 1.1.0 (rebrand ADR-065 + estatística) — 2026-06-22 · Todos os direitos reservados.*
