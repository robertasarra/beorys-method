# BEORYS™ — Registro Público de Autoria e Método

**BEORYS™** é uma obra e metodologia proprietária de controle epistêmico de modelos de linguagem (LLMs), desenvolvida por Roberta Sarra España.

---

## Princípio fundador

> **"A fluência pode redigir; não pode autorizar."**

A tese central: o problema não é ensinar uma regra ao LLM; é obrigar que a verificação seja executada no momento correto. A solução defendida é separar produção de autorização — o LLM pode gerar, mas a autorização deve vir de verificação externa, determinística, auditável e de falha-fechada.

---

## O que é este repositório

Este repositório **não é um pacote reprodutível de implementação.** É um registro público de autoria, prioridade, fundamentação acadêmica, resultados agregados e integridade documental. A implementação, os prompts, os critérios de bloqueio, os scripts, o dataset integral e a lógica operacional permanecem protegidos como segredo industrial.

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

## Resultados agregados autorizados (BEORYS-PCT v0.2)

Benchmark comparativo entre 5 grupos de instrução (A a E), medindo compliance de protocolo em 100 casos, 7 categorias, 2.500 execuções:

| Grupo | Trigger Activation Rate | Auditability Score |
|---|---:|---:|
| A — Prosa | 2% | 0.60 |
| B — Checklist | 23% | 0.64 |
| C — Auto-reflexão | 23% | 0.66 |
| D — Executor + LLM-validador | 2% | 0.61 |
| **E — BEORYS™** | **93%** | **0.83** |

Tabela completa: [BEORYS_PCT_v0.2_RESULTS_TABLE.md](benchmark/BEORYS_PCT_v0.2_RESULTS_TABLE.md)

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

## Como citar

```
España, Roberta Sarra. BEORYS™: Metodologia de Controle Epistêmico de LLMs.
Registro público de autoria e prioridade. 2026.
https://github.com/robertasarra/beorys-method
```

Formato estruturado: [CITATION.cff](CITATION.cff)

---

## Integridade e auditoria

Os documentos públicos são cobertos por registro SHA-256 em [SHA256_REGISTRY.md](integrity/SHA256_REGISTRY.md). Um hash-mestre privado do run v0.2 foi gerado e está em custódia da titular para eventual auditoria independente sob NDA. Política completa: [HASH_POLICY.md](integrity/HASH_POLICY.md).

---

## Contato

Roberta Sarra España — titular exclusiva de todos os direitos sobre BEORYS™.
Para licenciamento, auditoria ou parceria: conforme [NOTICE.md](NOTICE.md).

---

*Versão pública: 1.0.0 — 2026-06-06*  
*Todos os direitos reservados. Nenhuma licença de uso da metodologia é concedida por este repositório.*
