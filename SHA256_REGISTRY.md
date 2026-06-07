# SHA256_REGISTRY — Registro de Integridade / Integrity Registry

**BEORYS™** — Metodologia de Controle Epistêmico de LLMs  
**Titular:** Roberta Sarra España  
**Data de anterioridade:** 2026-06-06  
**Versão do registro:** 1.0.0

---

## Política de integridade

Ver [HASH_POLICY.md](./HASH_POLICY.md) para descrição completa da política.

**Algoritmo:** SHA-256  
**Escopo:** Documentos públicos listados abaixo.  
**Nota:** Os hashes registrados aqui são os hashes **correntes** dos arquivos públicos neste repositório. Documentos privados (prompts, scripts, dataset, lógica de gate) são cobertos por hash-mestre separado, custodiado pela titular.

---

## Documentos públicos — hashes verificáveis

| Arquivo | SHA-256 |
|---|---|
| `README.md` | `35c256546a3de7420078bd58b3de7350182deef1542d2789011fefb9f47f5532` |
| `CLAIM-001.md` | `7b2bf7c7e211cffaf54cabe42c224143c212522a618267e26aa4696141b74ada` |
| `FUNDAMENTACAO_ACADEMICA.md` | `dda97785d9d29001c2c51a756d8731ce48ce94f40134b54fb6444d082ffe02fc` |
| `CITATION.cff` | `199d491e440b557d9bed0805accf6cbcc0b2cdaae9b73be71ed8c51ec6b37c74` |
| `LICENSE` | `a77da0521edad05bb806a19ef86410bbf31ddc8b90d89349f81aa16de229b7a1` |
| `NOTICE.md` | `03750a3af1e43d0eb73489b133f4752d0f27a98cdadb3d47206386bd73658eea` |
| `CHANGELOG.md` | `a12e2649f2fcdfa6aa11cc76bcc3e08ee443ac5693ed4ef9f4e1b81c10098705` |
| `TRADE_SECRET.md` | `d6c8d4911233af08ba913b3eb3ed8ae00307d44821d19d8ec34a91026fc39200` |
| `BEORYS_PCT_v0.2_METHOD.md` | `cb6bbecb39eb588b0cd6c2e155a702fda378e821a47d9ea579537075363d2a8c` |
| `BEORYS_PCT_v0.2_RESULTS_TABLE.md` | `11427c17e90dc5025d88472a8ae107557abc11a5c589f76ae4645b0313f5473f` |
| `BEORYS_PCT_v0.2_VALIDATION_REPORT.md` | `e84fd65338d96001e9602b04fcd0731d895b0a3c4fb8f5cb2855ff81a7a882e7` |
| `BEORYS_PCT_v0.2_EVIDENCE_CHECKLIST.md` | `92530d61d12322299e164bf7e5ac4cbe30043b4027a63e4750116a79cdca619e` |
| `BEORYS_PCT_v0.2_LIMITATIONS.md` | `9a269298a5b263af41baf22eeccef56e6e1d8a3d42217c797c936d5952e34a45` |
| `BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md` | `be4ecc7146269cbd3685216c835527b978b3de1233306d3ca48f27c8a4ba20c6` |
| `BEORYS_PCT_v0.2_PUBLIC_SUMMARY.md` | `c914aac423e67761514f4e3bc7c87efab2b0fa4f9162700376db51210859f19e` |
| `BEORYS_PCT_v0.2_SUMMARY.md` | `bada8fbae3287ef8ca9109ad75bbe112d783148e009a230c2ddc32e5a4b188a1` |
| `REFERENCES.md` | `ab71fbff0906b3250a543148977daee49abaa58b43fd002b405f5fffbfcbf79d` |
| `LITERATURE_MAP.md` | `9f828eff1e0ff64239aa5b09db69b683c3fa0377b624af00a5cddd95aadf5b7b` |
| `HASH_POLICY.md` | `0561010a09339739e1e5988a2d668720f3cda9e168c19d3466d132bf022ffe2c` |
| `RELEASE_INTEGRITY.md` | `132884233dfa4a4ccd400ceaa5052b3568ca175325dba4120ea268404eea4d2f` |

---

## Hash-mestre privado — BEORYS-PCT v0.2

O hash-mestre do pacote privado completo (prompts, scripts, dataset, lógica de gate) é custodiado exclusivamente pela titular e não é publicado neste repositório.

**Referência:** a fornecer pela titular em instância de verificação formal.

---

## Verificação

Para verificar qualquer arquivo listado acima:

```bash
shasum -a 256 <nome-do-arquivo>
```

O hash retornado deve corresponder ao valor registrado na tabela acima.

---

## Aviso

Este registro documenta a integridade dos documentos públicos no momento do commit.  
Qualquer divergência entre o hash calculado e o registrado indica que o arquivo foi alterado após a publicação.

**© 2026 Roberta Sarra España — Todos os direitos reservados**
