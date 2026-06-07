# SHA256_REGISTRY — Registro de Integridade - Integrity Registry

| | |
|---|---|
| **Obra / Work** | BEORYS™ |
| **Autora / Author** | Roberta Sarra España |
| **Versão do registro / Record version** | 1.0.2 |
| **Recomputado em / Recomputed** | 2026-06-06 23:57:43 -03 |
| **Algoritmo / Algorithm** | SHA-256 |

> Registro corrente dos hashes dos documentos públicos canônicos. Política em
> [`HASH_POLICY.md`](./HASH_POLICY.md). Recalculado a cada versão do
> [`CHANGELOG.md`](../CHANGELOG.md). O próprio `SHA256_REGISTRY.md` não se
> auto-inclui.

---

## 1. Documentos públicos canônicos

| Arquivo | SHA-256 |
|---|---|
| `CHANGELOG.md` | `1a946200a71853e68c793e526031485f348be30d21e0cd08ac46752034063d71` |
| `CITATION.cff` | `29bfa72c74949a897669a78ade9bcb5b2cfbc8222f599b324952e6124cd5935b` |
| `CLAIM-001.md` | `ee7a8e4532710df90568825416d72aa21aeac23d11c6e1c2708acae8bd483146` |
| `FUNDAMENTACAO_ACADEMICA.md` | `c7e1cdade81450f75b0f0d51ce22c2073d08a8ae1d188eaa7a9862fcbde8822a` |
| `LICENSE` | `ff5610fcf7b26bf8a5ed3eccaf21e438d812c68cba2ed5f2fe5af438bd336f8a` |
| `NOTICE.md` | `c9e60720d7c221c704253595142ec76ce5a03e087c28d7d0aa4c8925166a99d6` |
| `README.md` | `ad4f83ad35bd792efc5fd41a82d8f6e87f179dd90b244ecabfec6a90336268ef` |
| `TRADE_SECRET.md` | `f6657b13112e2aad400e8ee703d3e112c960c2589d015a8cab8695b96b562c61` |
| `docs/benchmark/BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md` | `f5b12e9e2cea3a762e7ce9b936903d6bba052e6c2ac3900f1506c523ab20fe45` |
| `docs/benchmark/BEORYS_PCT_v0.2_LIMITATIONS.md` | `c5f7d3a4a1e863773b5b2c0c62d0932644a5bfa116d16808ab684b056133af9d` |
| `docs/benchmark/BEORYS_PCT_v0.2_METHOD.md` | `4f045d1454100fe80e116c28f114f407406b559036019c0da7988ec38ca652bb` |
| `docs/benchmark/BEORYS_PCT_v0.2_PUBLIC_SUMMARY.md` | `7fc9af5157e21e7c78977366f1e0d5714df006614c2fa5f780e131419bf1bcd1` |
| `docs/benchmark/BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md` | `166e15f68b3e551d92592095b80dc6585504ab273796a9037650e40a5d55d60e` |
| `docs/benchmark/BEORYS_PCT_v0.2_RESULTS_TABLE.md` | `ed53e35bca012a739cae95b9f8d499029c8d11e1b82731059e64d9e0e43e6be4` |
| `docs/benchmark/BEORYS_PCT_v0.2_SUMMARY.md` | `cac0fce6d2ca8792348f7009f7fdb08c02e6bc2d6c336c0bb9dc0a61c505561e` |
| `docs/benchmark/BEORYS_PCT_v0.2_VALIDATION_REPORT.md` | `1f5cccd51efd6f56a1806721a2e0814434f10e4da10dd23c1ef7e77c847670cf` |
| `docs/claims/CLAIM-001.md` | `d42002d2fb32a50a92797f2382781874747f092c47a3ff0b9be2b479f943bff5` |
| `docs/literature/LITERATURE_MAP.md` | `6b6605f209faf9c41204d8e189fbcdef3a34685965bfdcc695d63240c30b3e80` |
| `docs/literature/REFERENCES.md` | `f3ed4669aa6220c18743bb098def098e91c337b3fef22b68a7fc1f4a86d32938` |
| `integrity/HASH_POLICY.md` | `500ee4dbea90d4e873058aad363d3826577ad8f04497f16f27eef8844c739935` |
| `integrity/RELEASE_INTEGRITY.md` | `077e34203db32f4ba50544380e02032c026d841ac10c9d139db0eca61cf12baa` |

## 2. Benchmark v0.2 — hash-mestre (fonte bruta de uso controlado)

A fonte bruta do run v0.2 (**não** publicada — ver
[`../TRADE_SECRET.md`](../TRADE_SECRET.md)) é selada por um hash-mestre SHA-256, que
fixa publicamente a sua existência e forma exata sem revelar conteúdo:

| Item | SHA-256 |
|---|---|
| Hash-mestre do run v0.2 (manifesto `SHA256SUMS.txt`, 5.533 arquivos) | `ebfc9db96869484987f165ab74f515fa76600b945e6dc5852f9c77aa273d56f2` |

## 3. Como verificar / How to verify

```
# a partir desta pasta (registro-publico-beorys/):
sha256sum CLAIM-001.md   # compare com a linha correspondente acima
```

Qualquer divergência indica que o arquivo foi alterado após o registro.

---

© 2026 Roberta Sarra España — BEORYS™. Ver [`LICENSE`](../LICENSE).
