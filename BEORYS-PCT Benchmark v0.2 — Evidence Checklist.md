# BEORYS-PCT Benchmark v0.2 — Evidence Checklist

| | |
|---|---|
| **Work** | BEORYS™ |
| **Author** | Roberta Sarra España |
| **Run** | BEORYS-PCT Benchmark v0.2 — 2026-06-06 |
| **Boundary** | Public evidence record. No implementation disclosed — see [`../../TRADE_SECRET.md`](../../TRADE_SECRET.md). |

---

## 1. Public Evidence

Publicly available, aggregate and high-level: the benchmark identifier and date, the
number of executions, the model list, the group definitions (high-level only) and the
aggregate metrics published in
[`BEORYS_PCT_v0.2_RESULTS_TABLE.md`](./BEORYS_PCT_v0.2_RESULTS_TABLE.md).

## 2. Protected Evidence

Held as trade secret and **not** published: the full prompts, the full dataset, the
gate implementation, the internal scripts, the complete blocking criteria, the
proprietary heuristics and the complete operational flow.

## 3. Integrity Evidence

Integrity of the run's raw evidence (controlled, not public) is sealed by a SHA-256
**master hash**; the policy is in
[`../../integrity/HASH_POLICY.md`](../../integrity/HASH_POLICY.md) and the current
public hashes in [`../../integrity/SHA256_REGISTRY.md`](../../integrity/SHA256_REGISTRY.md).

## 4. Missing or Non-Public Evidence

Anything not listed as public in §1 is, by design, **non-public**. The absence of a
given artifact from the public record is intentional and reflects the disclosure
boundary, not a gap in the run.

## 5. Disclosure Boundary

The public record discloses **aggregate method and results only**. The publication of
this repository does not constitute disclosure of the implementation.

---

## Evidence table

| Evidence Item | Status | Public? | Notes |
|---|---|---|---|
| Benchmark name | Available | YES | Public identifier |
| Execution date | Available | YES | 2026-06-06 |
| Number of executions | Available | YES | 2,500 |
| Model list | Available | YES | Public aggregate |
| Group definitions | Available | YES | High-level only |
| Aggregate metrics | Available | YES | Published summary |
| Full prompts | Withheld | NO | Protected |
| Full dataset | Withheld | NO | Protected |
| Gate implementation | Withheld | NO | Protected |
| Internal scripts | Withheld | NO | Protected |

---

© 2026 Roberta Sarra España — BEORYS™. See [`LICENSE`](../../LICENSE).
