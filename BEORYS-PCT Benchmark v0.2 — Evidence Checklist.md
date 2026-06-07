# BEORYS-PCT v0.2 — Checklist de Evidência

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Titular:** Roberta Sarra España

Este documento separa explicitamente o que é evidência pública, o que é evidência protegida e o que é evidência selada (em custódia da titular).

---

## 1. Evidência pública

Disponível neste repositório, citável com atribuição:

| Evidência | Status | Localização |
|---|---|---|
| Data de execução do run | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Número de modelos avaliados (5) | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Número de casos (100) | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Número de categorias (7) | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Número de execuções (2.500) | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Grupos avaliados (A–E) e seus tipos | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Métricas utilizadas (nomes) | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Tabela de resultados agregados | ✅ público | (BEORYS-PCT Benchmark v0.2 — Results Table) |
| Princípio de medição (first-attempt, deterministic, anticircular) | ✅ público | (BEORYS-PCT Benchmark v0.2 — Method) |
| Declaração de limitações | ✅ público | (BEORYS-PCT Benchmark v0.2 — Limitations.md) |
| Declaração de reprodutibilidade parcial | ✅ público | (BEORYS-PCT Benchmark v0.2 — Reproducibility Statement.md) |
| Hashes SHA-256 dos documentos públicos | ✅ público | integrit(./SHA256_REGISTRY — Registro de Integridade - Integrity Registry.md) |

---

## 2. Evidência protegida (segredo industrial — não publicada)

| Evidência | Status | Razão |
|---|---|---|
| Identidade individual dos modelos avaliados | 🔒 protegida | Ativo de avaliação proprietário |
| Conjunto de casos (tarefas individuais) | 🔒 protegida | Dataset proprietário |
| Verdades-base das tarefas | 🔒 protegida | Critério de avaliação proprietário |
| Saídas brutas dos modelos (outputs individuais) | 🔒 protegida | Evidência bruta proprietária |
| Prompts internos de cada grupo (A–E) | 🔒 protegida | Propriedade intelectual central |
| Critérios operacionais do verificador | 🔒 protegida | Núcleo do gate BEORYS™ |
| Thresholds e condições de bloqueio | 🔒 protegida | Segredo industrial |
| Scripts de pipeline e orquestração | 🔒 protegida | Implementação proprietária |
| Logs completos do run | 🔒 protegida | Evidência bruta |
| Análise por modelo individual | 🔒 protegida | Granularidade proprietária |
| Análise por categoria individual | 🔒 protegida | Granularidade proprietária |

---

## 3. Evidência selada (em custódia da titular)

| Evidência | Status | Descrição |
|---|---|---|
| Hash-mestre privado do run v0.2 | 🔐 selada | SHA-256 do conjunto completo: dataset + outputs + logs + configuração; disponível para auditoria independente sob NDA |

---

## 4. Consequência

A evidência pública é suficiente para:
- Verificar autoria e prioridade
- Citar resultados agregados com atribuição correta
- Comparar grupos A–E a nível de métricas agregadas
- Verificar integridade dos documentos públicos

A evidência pública **não é suficiente** para:
- Reproduzir o experimento integralmente
- Auditar casos individuais
- Verificar a correção de pontuações individuais
- Contestar resultados com granularidade acima do nível agregado

Para auditoria com evidência bruta, contatar a titular para acordo formal sob NDA.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
