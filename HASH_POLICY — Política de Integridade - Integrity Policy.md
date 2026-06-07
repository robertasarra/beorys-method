# HASH_POLICY — Política de Integridade - Integrity Policy

| | |
|---|---|
| **Obra / Work** | BEORYS™ |
| **Autora / Author** | Roberta Sarra España |
| **Registro público / Public record** | 2026-06-06 |
| **Algoritmo / Algorithm** | SHA-256 |

---

# 🇧🇷 Português

## 1. Por que SHA-256

A integridade dos documentos públicos é fixada com **SHA-256** (família SHA-2). A
escolha é deliberada:

- é um padrão criptográfico **amplamente adotado e auditável** por terceiros, sem
  depender de nenhuma ferramenta proprietária;
- qualquer alteração de **um único byte** em um arquivo muda completamente o seu
  hash, tornando adulterações **detectáveis**;
- o cálculo é **reproduzível** em qualquer sistema (`sha256sum`, `shasum -a 256`,
  bibliotecas padrão), o que permite a verificação independente por qualquer parte.

O objetivo **não** é sigilo (um hash não esconde conteúdo) — é **prova de
integridade e datação**: demonstrar que um documento existia, naquela forma exata,
na data registrada.

## 2. Quais documentos são canônicos

São canônicos, para fins de integridade, os **documentos públicos** deste
repositório:

- `README.md`, `CLAIM-001.md`, `FUNDAMENTACAO_ACADEMICA.md`;
- `NOTICE.md`, `TRADE_SECRET.md`, `LICENSE`;
- `CHANGELOG.md`, `CITATION.cff`;
- os documentos em `integrity/`, `docs/benchmark/`, `docs/literature/` e
  `docs/claims/`.

O **registro corrente** dos hashes desses arquivos está em
[`SHA256_REGISTRY.md`](./SHA256_REGISTRY.md). A fonte bruta do benchmark **não** é
publicada aqui (ver [`TRADE_SECRET.md`](../TRADE_SECRET.md)); dela só se publica,
quando aplicável, o **hash-mestre**, nunca o conteúdo.

## 3. Quando os hashes são atualizados

Os hashes em [`SHA256_REGISTRY.md`](./SHA256_REGISTRY.md) são recalculados e
republicados **sempre que** um documento canônico muda — ou seja, a cada nova
versão registrada no [`CHANGELOG.md`](../CHANGELOG.md). Cada atualização:

1. registra a **data** da recomputação;
2. associa os hashes à **versão** correspondente do registro público;
3. **preserva** o histórico anterior (os hashes antigos não são apagados do
   histórico do repositório).

## 4. Integridade e rastreabilidade

Integridade e rastreabilidade são complementares:

- a **integridade** (este documento) responde *"este arquivo foi alterado?"*;
- a **rastreabilidade** (CHANGELOG + histórico de versões) responde *"o que mudou,
  quando e por quê?"*.

Juntas, elas tornam o registro público **defensável**: qualquer auditor pode
confirmar tanto o conteúdo exato de cada documento quanto a sua evolução datada.

---

# 🌎 English (short version)

Integrity of the public documents is fixed with **SHA-256**: a widely adopted,
auditable cryptographic standard, reproducible on any system, where a single-byte
change fully alters the hash. The goal is **not** secrecy but **proof of integrity
and dating**. The **canonical** documents are this repository's public files
(README, CLAIM, academic foundation, NOTICE, TRADE_SECRET, LICENSE, CHANGELOG,
CITATION, and the `integrity/`, `docs/benchmark/`, `docs/literature/`,
`docs/claims/` files); their current hashes are in
[`SHA256_REGISTRY.md`](./SHA256_REGISTRY.md). Hashes are recomputed **whenever a
canonical document changes** (i.e., at each `CHANGELOG` version), recording the date
and preserving prior history. Integrity answers *"was this file altered?"*;
traceability (CHANGELOG + version history) answers *"what changed, when, and why?"*.
The raw benchmark data is **not** published here; only its master hash may be, never
its content.

---

© 2026 Roberta Sarra España — BEORYS™. Ver [`LICENSE`](../LICENSE).
