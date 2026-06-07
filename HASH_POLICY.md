# HASH_POLICY — Política de Integridade SHA-256

**BEORYS™** | Versão pública: 1.0.0 | Titular: Roberta Sarra España

---

## 1. Algoritmo

Todos os hashes de integridade neste repositório usam **SHA-256** (Secure Hash Algorithm 256-bit).

---

## 2. Escopo dos hashes públicos

Os hashes em `SHA256_REGISTRY.md` cobrem **apenas os documentos públicos deste repositório**. Calculados sobre o conteúdo do arquivo (bytes brutos, sem normalização de line endings).

Cada linha do registro segue o formato:
```
SHA256:<hash_hex>  <caminho_relativo_ao_repositorio>
```

---

## 3. Auto-exclusão

`SHA256_REGISTRY.md` **não se inclui** no próprio registro — calcular o hash de um arquivo que lista seu próprio hash é circularmente indefinido. `RELEASE_INTEGRITY.md` e `HASH_POLICY.md` também são excluídos do registro pelos mesmos motivos.

---

## 4. Quando recalcular hashes

Os hashes devem ser recalculados e atualizados em `SHA256_REGISTRY.md` sempre que:
- Um documento público for editado
- Um novo documento público for adicionado
- Um documento público for renomeado ou removido

Após cada recalculo, `RELEASE_INTEGRITY.md` deve ser atualizado com a nova data.

---

## 5. Como verificar

Para verificar a integridade de um documento público:

```bash
# Em sistemas Unix/macOS:
sha256sum <arquivo>
# ou
shasum -a 256 <arquivo>

# Em Windows (PowerShell):
Get-FileHash <arquivo> -Algorithm SHA256
```

Compare o hash obtido com o valor em `SHA256_REGISTRY.md`. Divergência indica alteração do documento após a publicação do registro.

---

## 6. Hash-mestre privado do run BEORYS-PCT v0.2

Existe um **hash-mestre privado** do run v0.2, calculado sobre o conjunto completo: dataset + outputs brutos + logs de execução + configuração. Este hash:

- **Não está publicado** neste repositório
- Está em **custódia exclusiva da titular** (Roberta Sarra España)
- Pode ser verificado por auditor independente sob NDA formal
- Constitui a âncora de integridade para auditoria da evidência bruta

O hash-mestre privado e os hashes dos documentos públicos servem propósitos distintos:
- Hashes públicos: verificar que os documentos públicos não foram alterados após publicação
- Hash-mestre privado: verificar que a evidência bruta protegida corresponde ao que foi declarado publicamente

---

## 7. Limitação

O registro de hashes públicos garante integridade documental — não autenticidade de origem. Para verificação de autoria, o registro de commits do GitHub (com timestamps) é a fonte primária.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
