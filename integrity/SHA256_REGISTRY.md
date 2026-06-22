# SHA256_REGISTRY — Registro de Integridade / Integrity Registry

**BEORYS™** — Metodologia de Controle Epistêmico de LLMs  
**Titular:** Roberta Sarra España  
**Data de anterioridade:** 2026-06-06  
**Atualizado em:** 2026-06-22 (versão pública 1.1.0)  
**Versão do registro:** 2.1.0

---

## Política de integridade

Ver [HASH_POLICY.md](./HASH_POLICY.md) para descrição completa da política.

**Algoritmo:** SHA-256  
**Escopo:** Documentos públicos listados abaixo.  
**Auto-exclusão:** O próprio `integrity/SHA256_REGISTRY.md` não está incluído na tabela — incluir o hash de um arquivo dentro dele mesmo cria dependência circular irresolvível. O hash do registro é publicado após o commit em seção separada abaixo.  
**Nota:** Documentos privados (prompts, scripts, dataset, lógica de gate) são cobertos por hash-mestre separado, custodiado exclusivamente pela titular.

---

## Documentos públicos — hashes verificáveis

| Arquivo | SHA-256 |
|---|---|
| `README.md` | `a04851f52a44e5485bbce283f5c6b3f57ee73f8ba7a599c10eca000c817648cc` |
| `LICENSE.md` | `a77da0521edad05bb806a19ef86410bbf31ddc8b90d89349f81aa16de229b7a1` |
| `NOTICE.md` | `9130b4ebfb35aa2b544ba9519b1ac5731c314ed43ec817c6e7c36c56efe53868` |
| `CITATION.cff` | `199d491e440b557d9bed0805accf6cbcc0b2cdaae9b73be71ed8c51ec6b37c74` |
| `CHANGELOG.md` | `8a65872ce38fcf6b71404ef5baa6750e51278e4f27ba334424906a77c2f108c4` |
| `claims/CLAIM-001.md` | `7b2bf7c7e211cffaf54cabe42c224143c212522a618267e26aa4696141b74ada` |
| `benchmark/BEORYS_PCT_v0.2_PUBLIC_SUMMARY.md` | `985f1cd4ec783441f302a995dad2be45a429407b93d54f79155f8fd73299f33f` |
| `benchmark/BEORYS_PCT_v0.2_AGGREGATE_SUMMARY.md` | `f0ccbb244bc685b29438bc17bfc91570f4dae4bfdeab329762d7d789870aad46` |
| `benchmark/BEORYS_PCT_v0.2_METHOD.md` | `cb6bbecb39eb588b0cd6c2e155a702fda378e821a47d9ea579537075363d2a8c` |
| `benchmark/BEORYS_PCT_v0.2_RESULTS_TABLE.md` | `38c07ce90a4ed480eedf3ed54ebd6c18ff9d7296e8c29e72ae1d1a10a556a138` |
| `benchmark/BEORYS_PCT_v0.2_STATISTICS.md` | `c42f69bb69006810083e95521dd1fb7c8c86c22b77e06dd64cccdb9084e532a8` |
| `benchmark/BEORYS_PCT_v0.2_MODELS.md` | `38ffa27832ad845713dca33c3413f2306eb52b6a201a89d11de20d3a050df96b` |
| `benchmark/BEORYS_PCT_v0.2_VALIDATION_REPORT.md` | `8c4c4025a41ebf4d1f68d4d96eb596f74f5bab930ef2a1d8dfffbbdc654e2a84` |
| `benchmark/BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md` | `ac1e65e93d7fda48084c24871beb1bba53201264e39e1aa66f2e245de922bd4a` |
| `benchmark/BEORYS_PCT_v0.2_LIMITATIONS.md` | `0d2a0739d9d12f93202055e99807e26848585b8c89d3bc02cd2131db003f9aab` |
| `benchmark/BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md` | `9be65bddadc416407c31943865fe574c2718128c3d43d7327f239eefe859d903` |
| `literature/FUNDAMENTACAO_ACADEMICA.md` | `dda97785d9d29001c2c51a756d8731ce48ce94f40134b54fb6444d082ffe02fc` |
| `literature/REFERENCES.md` | `ab71fbff0906b3250a543148977daee49abaa58b43fd002b405f5fffbfcbf79d` |
| `literature/LITERATURE_MAP.md` | `9f828eff1e0ff64239aa5b09db69b683c3fa0377b624af00a5cddd95aadf5b7b` |
| `legal/TRADE_SECRET.md` | `84aab7927285e952419db6d4960c6da66034bf49c96fe331a5c8325bb9d21bcb` |
| `integrity/HASH_POLICY.md` | `5456b3a107e834306430fe9aebea69d7fee8581e172067a81f3dc08ede09d492` |
| `integrity/RELEASE_INTEGRITY.md` | `fd8df07614aebcd936e84caa1156f78473fc2d6e42ec09d410ec9c91dd73165c` |

---

## Hash do registro após publicação

> **A ser preenchido pela titular após o commit final.**  
> Procedimento: após `git push`, executar `shasum -a 256 integrity/SHA256_REGISTRY.md` e registrar o resultado aqui em commit de anotação separado.

---

## Hash-mestre privado — BEORYS-PCT v0.2

O hash-mestre do pacote privado completo (prompts, scripts, dataset, lógica de gate) é custodiado exclusivamente pela titular e não é publicado neste repositório.

**Referência:** a fornecer pela titular em instância de verificação formal sob NDA.

---

## Verificação

Para verificar qualquer arquivo listado acima:

```bash
shasum -a 256 <caminho-do-arquivo>
```

O hash retornado deve corresponder ao valor registrado na tabela acima.

---

**© 2026 Roberta Sarra España — Todos os direitos reservados**
