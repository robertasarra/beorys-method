# BEORYS-PCT v0.2 — Relatório de Validação Pública

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## 1. Declaração de validação

O BEORYS-PCT v0.2 foi conduzido sob as seguintes condições, declaradas publicamente para fins de registro de autoria e prioridade:

| Condição | Declaração |
|---|---|
| Conjunto de casos | O mesmo conjunto de 100 casos foi aplicado a todos os 5 grupos (A–E) |
| Verificador | O mesmo verificador determinístico foi usado para todos os grupos |
| Parâmetros de modelo | Os mesmos parâmetros de temperatura e configuração foram aplicados a todos os grupos |
| Ordem de avaliação | Grupos avaliados de forma independente; sem contaminação cruzada |
| Medição | Compliance de primeira saída; sem reapresentação ou reformulação |

---

## 2. O que esta validação afirma

- Que os resultados agregados publicados na [tabela de resultados]((BEORYS_PCT_v0.2_RESULTS_TABLE.md))) refletem a execução do benchmark nas condições declaradas.
- Que a diferença entre grupos (especialmente Trigger Activation Rate: 2% em A vs. 93% em E) é resultado das condições experimentais controladas.
- Que o verificador é externo e determinístico — não é o mesmo modelo sendo avaliado.

---

## 3. O que esta validação não afirma

- **Universalidade:** estes resultados não constituem prova de que o Grupo E supera os demais em todos os domínios, conjuntos de tarefas ou modelos.
- **Reprodutibilidade plena:** a reprodução integral do experimento requer acesso ao dataset, prompts e verificador protegidos — ver [(BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md)]((BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md))).
- **Significância estatística publicada:** análise estatística formal das diferenças entre grupos não está publicada nesta versão.
- **Veracidade factual:** o benchmark mede compliance estrutural de protocolo contra verdade-base das tarefas — não veracidade factual de evidências criadas livremente pelo modelo.

---

## 4. Evidência de integridade

A integridade dos documentos públicos é coberta por registro SHA-256 em [integri(../integrity/(../integrity/SHA256_REGISTRY.md))](../integrity/(../integrity/SHA256_REGISTRY.md))).

A titular mantém em custódia privada:
- Hash-mestre do run v0.2 (cobrindo dataset, outputs brutos, logs e configuração completa)
- Evidências brutas para eventual auditoria independente sob NDA

---

## 5. Conclusão

Os resultados agregados publicados são considerados válidos dentro do escopo declarado: 5 modelos, 100 casos, 7 categorias, 2.500 execuções, grupos A–E, condições constantes, verificador único determinístico externo.

Qualquer afirmação mais ampla derivada destes resultados é de responsabilidade de quem a fizer.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
