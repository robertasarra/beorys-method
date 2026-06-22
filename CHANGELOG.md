# CHANGELOG — BEORYS™ Repositório Público

Formato: [Versão] — Data — Descrição

---

## [1.1.0] — 2026-06-22 — Estatística + rebrand

### Adicionado
- `(benchmark/BEORYS_PCT_v0.2_STATISTICS.md)` — significância estatística e intervalos de confiança (IC 95% por escore de Wilson; testes z de duas proporções). Compliance bruta empata (E 95% × Prosa 95%, p = 1.00); o diferencial — com significância — é Trigger Activation (E 93% vs. baseline 23%; z = 22.4, p ≈ 2.3 × 10⁻¹¹¹), False Pass 0% por design, Unauthorized Output (E 2% vs. B 6%; p = 0.001) e Auditability 0.83
- `(benchmark/BEORYS_PCT_v0.2_MODELS.md)` — nomes e provedores dos 5 modelos avaliados (gpt-4o-mini, claude-haiku-4.5, gemini-3.5-flash, llama-3.3-70b-instruct, deepseek-chat-v3.1)

### Alterado
- `(README.md)` — passa a liderar pela métrica correta (compliance empata; o diferencial é onde a verificação dispara, não aprovar o inválido e auditabilidade); modelos nomeados; alinhado ao rebrand "Plano de Controle para Trabalho com IA / Continuidade · Autorização · Prova" (ADR-065)
- `(benchmark/BEORYS_PCT_v0.2_LIMITATIONS.md)` — limitação #4 (sem significância estatística) reclassificada como **parcialmente resolvida**; estabilidade temporal segue pendente
- `(integrity/SHA256_REGISTRY.md)` — hashes recalculados para arquivos novos e alterados
- `(integrity/RELEASE_INTEGRITY.md)` — versão pública 1.1.0 e lista de arquivos atualizadas

### Declarações
- Nenhum segredo industrial foi incluído nesta versão: dataset, prompts, thresholds e lógica de gate permanecem protegidos

---

## [1.0.0] — 2026-06-06 — Publicação inicial

### Criado
- `(README.md)` — porta de entrada do repositório público; sumário de documentos, resultados agregados, declaração de fronteiras e instruções de citação
- `(claims/CLAIM-001.md)` — declaração pública de autoria e prioridade (raiz e docs/claims/)
- `(literature/FUNDAMENTACAO_ACADEMICA.md)` — embasamento em literatura revisada por pares e preprints verificados
- `(CITATION.cff)` — metadados de citação no formato Citation File Format
- `LICENSE` — termos de uso do repositório público (todos os direitos reservados)
- `(NOTICE.md)` — declaração formal de direitos e proibições expressas
- `(legal/TRADE_SECRET.md)` — fronteira explícita entre público e segredo industrial
- `(CHANGELOG.md)` — este arquivo

### Criado — docs/benchmark/
- `(benchmark/BEORYS_PCT_v0.2_METHOD.md)` — declaração de método em alto nível (sem implementação)
- `(benchmark/BEORYS_PCT_v0.2_RESULTS_TABLE.md)` — tabela de resultados agregados autorizados
- `(benchmark/BEORYS_PCT_v0.2_VALIDATION_REPORT.md)` — relatório de validação pública agregada
- `(benchmark/BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md)` — checklist de evidência pública vs. protegida vs. selada
- `(benchmark/BEORYS_PCT_v0.2_LIMITATIONS.md)` — limitações declaradas do benchmark
- `(benchmark/BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md)` — declaração de reprodutibilidade parcial
- `(benchmark/BEORYS_PCT_v0.2_PUBLIC_SUMMARY.md)` — sumário público narrativo
- `(benchmark/BEORYS_PCT_v0.2_AGGREGATE_SUMMARY.md)` — sumário executivo

### Criado — docs/literature/
- `(literature/REFERENCES.md)` — lista de referências acadêmicas verificadas
- `(literature/LITERATURE_MAP.md)` — mapa afirmação → fonte

### Criado — integrity/
- `(integrity/HASH_POLICY.md)` — política de hashes SHA-256
- `(integrity/SHA256_REGISTRY.md)` — registro de hashes dos documentos públicos
- `(integrity/RELEASE_INTEGRITY.md)` — declaração de integridade desta versão

### Declarações
- Nenhum segredo industrial foi incluído nesta versão
- Nenhum prompt, script, critério de gate, dataset bruto ou lógica operacional foi publicado
- Todos os links internos foram verificados contra arquivos existentes

---

## Pendências dependentes da titular (ver [SHA256_REGISTRY.md](integrity/SHA256_REGISTRY.md))
- Hash-mestre privado do run BEORYS-PCT v0.2: a fornecer pela titular para inclusão em custódia declarada
