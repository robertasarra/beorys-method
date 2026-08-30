# GATE BEORYS — ADVERSARIAL ARCHITECTURE

Version: 1.0
Type: Repository-scoped adversarial architecture review skill
Mode: DOCUMENTATION-ONLY
Primary use: Vibe coding / AI-assisted software architecture
Implementation authorization: FORBIDDEN unless the user explicitly authorizes it after the final synthesis

## 1. PURPOSE

This skill creates a disciplined adversarial architecture process between two or more AI agents. The objective is not to make one AI win. The objective is to force competing architectural proposals to be tested against repository evidence and then combine the strongest verified elements into a better final decision.

Protocol: PROPOSAL → ADVERSARIAL CHALLENGE → REBUTTAL → SYNTHESIS.

Every phase must inspect the repository before concluding; anchor material claims in code evidence; distinguish FACT, INFERENCE, HYPOTHESIS and RECOMMENDATION; save a dated and signed document in the repository; change documentation only; report the saved path in chat; produce the exact handoff prompt for the next AI; and never implement or authorize implementation automatically.

## 2. NON-NEGOTIABLE RULES

### 2.1 Documentation-only gate

The agent MAY read source code, tests, configuration, infrastructure definitions, documentation, Git history, branches, PRs and issues when available, and create/edit only review documentation.

The agent MUST NOT modify application source code, tests, dependencies, lockfiles, migrations, CI/CD workflows, infrastructure, environment configuration or secrets; merge branches/PRs; deploy; execute destructive commands; or authorize another agent to implement.

### 2.2 Main/default branch protection

Prefer a documentation-only branch named `docs/adversarial-architecture/<YYYYMMDD>-<topic-slug>` for each review. Never discard unrelated work.

### 2.3 Evidence before conclusion

No material architectural claim may be presented as fact without repository evidence. If evidence is incomplete, label the statement `INFERENCE` or `HYPOTHESIS`. Never fabricate line numbers, paths, functions, APIs, schemas or runtime behavior.

### 2.4 Snapshot integrity

Every review records repository, branch analyzed, commit SHA, ISO-8601 timestamp, and agent/model identifier when known. Evidence from different commits must not be silently mixed.

## 3. REVIEW DIRECTORY

For every architectural question create:

`docs/adversarial-architecture/<YYYY-MM-DD>/<topic-slug>/`

Required files:
- `00-context.md`
- `01-proposal.md`
- `02-challenge.md`
- `03-rebuttal.md`
- `04-synthesis.md`
- `EVIDENCE.md`
- `DECISION.md`

Do not rewrite an earlier phase after the next phase has started. Corrections go into a dated ERRATA section.

## 4. EVIDENCE STANDARD

Each material item receives an ID `EV-001`, `EV-002`, etc. Each item must contain claim supported; classification FACT/INFERENCE/HYPOTHESIS; repository; branch; commit SHA; file; symbol/function/class/module; lines or exact locator; relevant excerpt or concise behavior description; interpretation; architectural relevance; and confidence HIGH/MEDIUM/LOW.

Recommendations must never be presented as current-state facts.

## 5. PHASE 0 — CONTEXT CAPTURE

Create `00-context.md` with user question, decision, constraints, excluded scope, repository, default branch, review branch, analyzed commit SHA, relevant PRs/issues, runtime limitations, unresolved questions and definition of success. End with `STATUS: CONTEXT FROZEN`.

## 6. PHASE 1 — PROPOSAL

Create `01-proposal.md`. Investigate before designing.

Required sections: Executive conclusion; Current architecture; Evidence inventory; Problem definition; Root cause; Constraints; Proposed solution; Architecture changes proposed; Alternatives considered; Why the preferred solution wins; Risks; Failure modes; Migration/rollout concept; Observability; Security; Performance; Cost; Maintainability; Reversibility; Test strategy concept; Unknowns; Assumptions; Questions the challenger should attack.

Include at least one credible alternative and a 0–5 decision matrix covering correctness, architectural fit, simplicity, maintainability, testability, observability, security, performance, operational complexity, cost, migration risk, reversibility and vendor lock-in.

Self-critique must identify strongest part, weakest part, falsifying evidence and greatest uncertainty.

## 7. PHASE 2 — ADVERSARIAL CHALLENGE

Create `02-challenge.md`. The challenger MUST independently inspect the repository and must not rely only on the proposal text.

Required analysis: verdict; what the proposal got right/wrong; unsupported claims; missing evidence; hidden assumptions; architectural, security, performance, data-model, operations, migration/rollback, testing and cost blind spots; coupling/lock-in; failure scenarios; better alternatives; challenger preferred solution; why better; evidence comparison; revised matrix; required corrections; questions for rebuttal.

Explicitly identify Strengths, Weaknesses, Opportunities, Threats/Risks and Improvements.

Every rejection of a major claim requires contradictory evidence, proof of missing evidence, a concrete failure scenario, or a demonstrably superior alternative under the same constraints. Mere disagreement is not admissible.

## 8. PHASE 3 — REBUTTAL

Create `03-rebuttal.md`. Respond point by point with a table: Challenge ID | Accept/Reject/Partial | Evidence | Reasoning | Change to proposal.

Acknowledge valid errors explicitly. Rejected criticisms require evidence. New claims require new evidence IDs. The proposer may revise the architecture but must not overwrite the original proposal.

Close with what changed, remaining disputes, updated preferred solution, updated risk register, updated decision matrix, remaining unknowns and recommendation for synthesis.

## 9. PHASE 4 — SYNTHESIS

Create `04-synthesis.md`. The synthesizer acts as judge/integrator, not third advocate.

Required sections: Final verdict; agreements; disagreements; stronger evidence on each disputed point; best elements from Proposal, Challenge and Rebuttal; Combined architecture; deliberately rejected architecture; why combined solution is superior; evidence map; final decision matrix; risks accepted/mitigated/open; implementation preconditions; validation plan; rollback requirements; implementation gates; user decision required.

Prefer evidence over confidence; simpler architectures when outcomes are equivalent; reversible decisions under uncertainty; repository-native patterns over unnecessary new abstractions; explicit failure handling over optimistic assumptions.

## 10. DECISION FILE

Create `DECISION.md` with Status (PROPOSED/ACCEPTED/REJECTED/NEEDS-VALIDATION), Decision, Why, Evidence, Rejected alternatives, Preconditions, `Implementation authorized: NO`, `Authorized by: USER ONLY`, Date and Review case path.

Implementation remains unauthorized unless the user explicitly authorizes it.

## 11. SIGNATURE STANDARD

Every phase document ends with:

---
Review-Phase: <PHASE>
Repository: <owner/repo>
Analyzed-Branch: <branch>
Analyzed-Commit: <SHA>
Document-Path: <path>
Prepared-By: <AI agent/model if known>
Role: <PROPOSER | CHALLENGER | REBUTTAL | SYNTHESIZER>
Timestamp: <ISO-8601 with timezone>
Implementation-Authorized: NO
Signature-Type: Declarative AI audit signature
---

This is an audit declaration, not a cryptographic or human legal signature.

## 12. CHAT RETURN CONTRACT

After each phase return: STATUS; exact saved path; repository+branch+commit evidence snapshot; verdict (max 5 bullets); explicit no-code confirmation; and complete copy/paste NEXT HANDOFF for the next AI.

The handoff must include repository, branch/commit, review case path, previous-phase path, required output path, instruction to independently inspect repository, documentation-only restriction, evidence standard, analytical role, save/date/sign requirement, and requirement to return the next handoff.

## 13. HANDOFF — CHALLENGER

You are the ADVERSARIAL ARCHITECTURE CHALLENGER. Independently inspect the repository and test the proposal against actual code evidence. Identify strengths, weaknesses, unsupported claims, hidden assumptions, failure modes, missed opportunities and superior alternatives. For every major criticism provide repository evidence or a concrete failure scenario. Save at `<REVIEW_CASE_PATH>/02-challenge.md`. Documentation-only. Date/sign. Return exact path, analyzed SHA, verdict, no-code confirmation and a complete rebuttal prompt targeting `<REVIEW_CASE_PATH>/03-rebuttal.md`.

## 14. HANDOFF — REBUTTAL

You are the ORIGINAL ARCHITECTURAL PROPOSER returning for REBUTTAL. Read proposal, challenge and evidence. Re-inspect repository evidence. Respond to every material challenge as ACCEPT, REJECT or PARTIAL, citing evidence and stating whether the architecture changes. Explicitly acknowledge valid errors and incorporate superior solutions. Save at `<REVIEW_CASE_PATH>/03-rebuttal.md`. Documentation-only. Date/sign. Return exact path, SHA, changes, unresolved disputes, no-code confirmation and a complete neutral synthesis prompt.

## 15. HANDOFF — SYNTHESIZER

You are the NEUTRAL ADVERSARIAL ARCHITECTURE SYNTHESIZER. Read all phase files and independently verify disputed points. Do not choose by rhetoric; choose by evidence strength. Combine the strongest validated elements. Save `<REVIEW_CASE_PATH>/04-synthesis.md` and `<REVIEW_CASE_PATH>/DECISION.md`. Implementation authorization remains NO. Documentation-only. Date/sign. Return paths, SHA, final verdict, combined architecture, remaining risks and explicit no-implementation status.

## 16. REQUIRED ADVERSARIAL QUESTIONS

Test architecture fit, duplicate mechanisms, unnecessary abstraction, coupling/global state; schema compatibility, reversibility, old data, consistency and idempotency; API contracts, failure propagation, retry/timeout/circuit breaking and lock-in; trust boundaries, authn/authz, secrets, injection/supply-chain/data exposure; concurrency, partial outage, scale, retry and restart failure; observability, rollback, diagnosis and operability; compute/storage/API/egress/human maintenance cost.

Vibe-coding-specific: challenge hallucinated framework capabilities, assumed absent APIs/functions, unnecessary generated abstraction, hidden dependencies, reviewability and whether the design is larger than the verified problem.

## 17. QUALITY GATES

A phase FAILS if it has material claims without evidence/classification; stale/mismatched commit evidence; invented file/line/symbol; source-code modification; implementation authorization without user approval; overwritten prior phase; challenger without independent repository inspection; rebuttal that ignores material items; synthesis that merely picks one side; missing saved path; missing next handoff; or missing date/signature.

## 18. FINAL PRINCIPLE

Attack the architecture. Then attack the attack. Finally combine what survives evidence.

The goal is not consensus. The goal is a better, evidence-backed, reversible architectural decision.
