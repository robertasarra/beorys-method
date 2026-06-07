# BEORYS-PCT v0.2 — Declaração de Reprodutibilidade

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## 1. Nível de reprodutibilidade pública

**Parcial — por design deliberado.**

A reprodutibilidade parcial é uma consequência direta da proteção de segredo industrial. Não é uma lacuna técnica nem um compromisso de publicação futura.

---

## 2. O que pode ser reproduzido publicamente

| Elemento | Reprodutível? | Observação |
|---|---|---|
| Desenho experimental de alto nível | ✅ Sim | 5 modelos, 100 casos, 7 categorias, grupos A–E, mesmas condições |
| Princípio de medição | ✅ Sim | First-attempt, deterministic verifier, anticircular |
| Resultados agregados publicados | ✅ Sim | Tabela em (BEORYS-PCT Benchmark v0.2 — Results Table) |
| Estrutura de métricas (nomes) | ✅ Sim | Listadas em (BEORYS-PCT Benchmark v0.2 — Method) |
| Experimento com design análogo usando recursos próprios | ⚠️ Parcialmente | Possível replicar o conceito com tarefas e prompts próprios; resultados não serão comparáveis diretamente |

---

## 3. O que não pode ser reproduzido sem acesso protegido

| Elemento | Reprodutível? | Razão |
|---|---|---|
| Dataset exato (100 casos com verdades-base) | ❌ Não | Segredo industrial |
| Prompts internos de cada grupo (A–E) | ❌ Não | Propriedade intelectual central |
| Verificador determinístico (scripts) | ❌ Não | Implementação proprietária |
| Critérios operacionais de compliance | ❌ Não | Núcleo do método |
| Run exato com os mesmos modelos nas mesmas versões | ❌ Não | Dataset + prompts protegidos |

---

## 4. Caminho de reprodutibilidade futura (auditoria)

A titular mantém em custódia privada:
- Hash-mestre SHA-256 do run v0.2 (cobrindo dataset + outputs + logs + configuração)
- Evidências brutas do run

Um **auditor independente qualificado** pode:
1. Assinar NDA formal com a titular
2. Receber acesso controlado às evidências brutas e ao verificador
3. Verificar que os resultados publicados correspondem às evidências protegidas
4. Emitir relatório de auditoria

Este caminho constitui o nível máximo de reprodutibilidade compatível com a proteção de segredo industrial.

---

## 5. Referência de benchmark para terceiros

Pesquisadores que desejem comparar seus próprios resultados com os do BEORYS-PCT v0.2 podem:
- Citar a tabela agregada pública com atribuição correta
- Conduzir seus próprios experimentos com métodos análogos aos grupos A–D (que são conhecidos da literatura) e comparar com os agregados publicados do Grupo E

A comparação direta com os dados brutos requer acordo de auditoria com a titular.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
