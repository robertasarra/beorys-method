# BEORYS-PCT Benchmark v0.2 — Resumo Agregado - Aggregate Summary

| | |
|---|---|
| **Obra / Work** | BEORYS™ |
| **Autora / Author** | Roberta Sarra España |
| **Run** | v0.2 — 2026-06-06 |
| **Escopo / Scope** | 5 modelos · 100 casos · 7 categorias · 2.500 execuções · 5 grupos (A–E) |

> Documento de **resultados agregados**. Não contém prompts, dataset, código,
> critérios de bloqueio ou qualquer implementação — ver
> [`TRADE_SECRET.md`](../../TRADE_SECRET.md).

---

# 🇧🇷 Português

## 1. O que o benchmark mede

O **BEORYS-PCT** (Protocol-Compliance Test) compara, no **mesmo** conjunto de casos
e modelos, **cinco formas de impor o mesmo protocolo**. A compliance é medida
sempre na **primeira saída** e julgada pelo **mesmo verificador determinístico**,
de forma anti-circular (a compliance da primeira saída é separada do bloqueio da
trava).

| Grupo | Mecanismo |
|---|---|
| A | Protocolo em prosa |
| B | Checklist estruturado |
| C | Autorreflexão |
| D | Executor + validador-LLM |
| E | BEORYS™ — gate de falha-fechada + trava externa |

## 2. Resultados agregados (únicos autorizados)

### 2.1 Compliance bruta da primeira saída

| Grupo | A | B | C | D | E |
|---|---:|---:|---:|---:|---:|
| Compliance | 95% | 93% | 92% | 93% | 95% |

Medida de forma justa, a compliance bruta **converge** (~92%–95%): a fluência, por
si só, já produz texto que **se lê** como conforme.

### 2.2 Métricas que separam o gate externo (E)

| Métrica | E | Comparação |
|---|---:|---|
| Acionamento do gatilho de verificação | 93% | vs **2%** (prosa) |
| Saída não-autorizada | 2% | a menor de todas |
| Aprovação falsa (*false pass*) | — | modo evitado; o validador-LLM (D) = **2%** |
| Auditabilidade (0–1) | 0,83 | vs **0,60** (prosa) |

> A tabela completa e oficial de métricas agregadas está em
> [`BEORYS_PCT_v0.2_RESULTS_TABLE.md`](./BEORYS_PCT_v0.2_RESULTS_TABLE.md).

## 3. Leitura dos resultados

A diferença decisiva **não** está na redação, e sim na **autorização**: o gate
externo aciona a verificação, barra a saída não-autorizada, não admite aprovação
falsa e é auditável. Os resultados observados são **consistentes com a hipótese**
de que a confiabilidade vem de uma verificação externa, determinística e de
falha-fechada — **nas condições medidas**.

## 4. Limites da evidência

- O run **descreve um conjunto específico de execuções**; **não** é prova universal
  e não generaliza automaticamente para outros modelos, domínios ou tarefas.
- Os resultados **não constituem prova definitiva**; novas replicações podem
  fortalecer, qualificar ou ajustar as conclusões.
- A fundamentação acadêmica completa está em
  [`../../FUNDAMENTACAO_ACADEMICA.md`](../../FUNDAMENTACAO_ACADEMICA.md) (§4, Limites
  da evidência) e o mapa literatura→hipótese em
  [`../literature/LITERATURE_MAP.md`](../literature/LITERATURE_MAP.md).

## 5. Integridade

A integridade do conjunto bruto de evidências do run (de uso controlado, **não**
publicado) é fixada por um **hash-mestre** SHA-256; a política está em
[`../../integrity/HASH_POLICY.md`](../../integrity/HASH_POLICY.md).

---

# 🌎 English (short version)

**BEORYS-PCT** (Protocol-Compliance Test) compares **five ways of enforcing the same
protocol** on the same cases and models, measuring compliance on the **first output**
with the **same deterministic verifier**, anti-circularly. v0.2 (2026-06-06): 5
models · 100 cases · 7 categories · 2,500 runs · groups A–E (A prose, B checklist,
C self-reflection, D executor + LLM validator, E BEORYS™ fail-closed gate + external
lock). **Raw first-output compliance** converges: A 95% · B 93% · C 92% · D 93% ·
E 95% — fluency alone already reads as compliant. The **external gate (E)** separates
on the other metrics: verification-trigger activation **93%** vs 2% (prose);
unauthorized output **2%** (lowest); false approval **0%** vs 2% (D); auditability
**0.83** vs 0.60 (prose). These observations are **consistent with the hypothesis**
that reliability comes from external, deterministic, fail-closed verification —
**under the measured conditions**. This is **not universal proof**; replications may
strengthen, qualify, or adjust the conclusions. No prompts, dataset, code, or
blocking criteria are disclosed (see [`TRADE_SECRET.md`](../../TRADE_SECRET.md)).

---

© 2026 Roberta Sarra España — BEORYS™. Ver [`LICENSE`](../../LICENSE).
