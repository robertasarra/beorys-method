# CHANGELOG — Registro público BEORYS™

Histórico das versões deste **registro público** (não da obra). O formato segue, de
forma simplificada, [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/), e
as datas estão em fuso de Brasília (BRT).

Este changelog cobre apenas os documentos públicos do repositório. Nenhuma entrada
descreve implementação, código, scripts ou conteúdo protegido — ver
[`TRADE_SECRET.md`](./TRADE_SECRET.md).

---

## [1.0.0] — 2026-06-06

### Adicionado
- **Registro público inicial** de autoria e prioridade do nome **BEORYS™** e da
  obra originária por trás dele.
- `CLAIM-001.md` — Declaração de Autoria e Prioridade (PT + EN), incluindo a
  estrutura canônica por nome (10 pilares, 14 regras LOCKED) e a evidência empírica
  agregada do **BEORYS-PCT Benchmark v0.2**.
- `README.md` — apresentação de alto nível da obra e da lacuna que ela endereça
  (PT + EN).
- `FUNDAMENTACAO_ACADEMICA.md` — literatura de referência conferida em fonte
  primária (DOI/arXiv) e evidência empírica agregada.
- `LICENSE` — todos os direitos reservados.
- `benchmark/` — pacote reprodutível público correspondente ao run **v0.1** (3
  métodos · 12 modelos · 576 execuções).

### Resultados agregados publicados (Benchmark v0.2 · 2026-06-06)
- 5 modelos · 100 casos · 7 categorias · 2.500 execuções · 5 grupos (A–E).
- Compliance bruta da 1ª saída: A 95% · B 93% · C 92% · D 93% · E 95%.
- Acionamento do gatilho de verificação: 93% (E) vs 2% (prosa).
- Saída não-autorizada: 2% (E). Aprovação falsa (false pass): validador-LLM (D) = 2%; o gate externo (E) evita o modo (—).
- Auditabilidade (0–1): 0,83 (E) vs 0,60 (prosa).

---

## [1.0.1] — 2026-06-07

### Corrigido
- Alinhamento da seção sobre a lacuna acadêmica, em `CLAIM-001.md` e `README.md`
  (PT + EN): a referência à literatura passou a apontar para o corpo de fontes
  conferidas (DOI/arXiv) em vez de citar um número fixo de estudos, eliminando uma
  inconsistência de contagem. Nenhum resultado ou afirmação foi alterado.

### Adicionado
- `NOTICE.md` — titularidade, natureza do repositório e ausência de concessão de
  direitos.
- `TRADE_SECRET.md` — delimitação explícita entre o que é público e o que
  permanece segredo industrial.
- `CHANGELOG.md` — este histórico.
- `CITATION.cff` — metadados de citação.

---

## [1.0.2] — 2026-06-07

### Alterado
- Revisão de defensabilidade científica em `CLAIM-001.md`, `README.md` e
  `FUNDAMENTACAO_ACADEMICA.md`: formulações absolutas substituídas por formulações
  cientificamente defensáveis (ex.: "já conhecem a regra" → "apresentaram evidência
  de conhecimento suficiente das regras testadas"; "resultado/demonstração empírica
  direta" → "os resultados observados são consistentes com a hipótese, nas condições
  medidas"). As duas frases canônicas do método foram **preservadas**. Nenhum número
  ou resultado foi alterado.

### Adicionado
- `README.md` — seção **Autorização vs. Fluência** (PT + EN).
- `FUNDAMENTACAO_ACADEMICA.md` — seção **Limites da evidência** (PT + EN).
- `NOTICE.md` — cláusulas explícitas: ler, clonar ou fazer fork **não** implicam
  autorização de uso; a implementação não está publicada.
- `TRADE_SECRET.md` — frase canônica "A publicação deste repositório não constitui
  divulgação da implementação."
- `integrity/HASH_POLICY.md`, `integrity/SHA256_REGISTRY.md`,
  `integrity/RELEASE_INTEGRITY.md` — política, registro e integridade de release.
- `docs/benchmark/BEORYS_PCT_v0.2_SUMMARY.md` — resumo agregado do benchmark v0.2.
- `docs/literature/REFERENCES.md` e `docs/literature/LITERATURE_MAP.md` — referências
  conferidas e mapa literatura→hipótese.
- `docs/claims/CLAIM-001.md` — ponteiro canônico para `../../CLAIM-001.md`.
- `docs/benchmark/` — conjunto documental completo do run **v0.2** (sem implementação):
  `BEORYS_PCT_v0.2_METHOD.md`, `..._VALIDATION_REPORT.md`, `..._EVIDENCE_CHECKLIST.md`,
  `..._LIMITATIONS.md`, `..._REPRODUCIBILITY_STATEMENT.md`, `..._PUBLIC_SUMMARY.md` e
  `..._RESULTS_TABLE.md` (tabela agregada oficial). Reformulação da linha de
  "aprovação falsa" para refletir a tabela oficial (D = 2%; E = —).

### Removido
- Cópias acidentais `README (copy).md` e `README (copy) 1.md` (duplicatas idênticas
  do `README.md`).

---

## English (short note)

This changelog tracks versions of the **public record**, not of the work itself.
**1.0.0 (2026-06-06):** initial public record of authorship and priority — CLAIM,
README, academic foundation, license, and the reproducible v0.1 benchmark package;
aggregate Benchmark v0.2 results published. **1.0.1 (2026-06-07):** academic-gap
reference aligned to the verified source list (no result changed); added NOTICE,
TRADE_SECRET, CHANGELOG, and CITATION. **1.0.2 (2026-06-07):** scientific-defensibility
pass over CLAIM, README, and the academic foundation (absolute wording softened; the
two canonical sentences preserved; no number changed); added the Authorization vs.
Fluency and Limits-of-the-evidence sections; added the `integrity/`, `docs/benchmark/`,
`docs/literature/`, and `docs/claims/` documents; removed accidental README copies.
Also added the full v0.2 benchmark document set under `docs/benchmark/` (method,
validation report, evidence checklist, limitations, reproducibility statement, public
summary, and the official aggregate results table), with no implementation disclosed.
