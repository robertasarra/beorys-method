# BEORYS-PCT v0.2 — Limitações Declaradas

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## Princípio de transparência

O BEORYS™ assume que declarar limitações é parte integral do método — não uma concessão retórica. Esta lista é exaustiva no que se refere ao registro público desta versão.

---

## Limitações

### 1. Não é prova universal

Os resultados do BEORYS-PCT v0.2 foram obtidos em condições específicas (5 modelos, 100 casos, 7 categorias, 1 run). Eles não constituem prova de que o Grupo E (BEORYS™) supera os demais métodos em:
- outros domínios de aplicação
- outros conjuntos de tarefas
- outros modelos de linguagem
- outras configurações de temperatura ou parâmetros
- outras línguas ou culturas de uso

---

### 2. Escopo limitado a um run

O BEORYS-PCT v0.2 é um único run executado em 2026-06-06. Sem repetição em múltiplas datas, os resultados não permitem afirmação sobre estabilidade temporal dos achados.

---

### 3. Sem generalização automática

A diferença observada entre grupos (especialmente Trigger Activation Rate: 2% em A vs. 93% em E) é válida dentro do escopo declarado. Qualquer generalização para além desse escopo é responsabilidade de quem a fizer — não da titular.

---

### 4. Significância estatística — **parcialmente resolvida**

A partir da versão pública 1.1.0, esta limitação está **parcialmente resolvida**. O documento [BEORYS_PCT_v0.2_STATISTICS.md](BEORYS_PCT_v0.2_STATISTICS.md) publica intervalos de confiança de 95% (escore de Wilson) e testes de significância (z de duas proporções, pooled) sobre os resultados agregados do run v0.2:

- **Trigger Activation** — E (93%) vs. melhor baseline (23%): z = 22.4, p ≈ 2.3 × 10⁻¹¹¹; ICs não sobrepostos.
- **Protocol Compliance** — E (95%) vs. Prosa (95%): z = 0.00, p = 1.00 (empate declarado explicitamente).
- **Unauthorized Output** — E (2%) vs. B (6%): z = −3.23, p = 0.001.
- **False Pass** — 0% por design em E vs. 2% em D.

**O que permanece pendente:** a análise cobre a significância das diferenças *dentro de um único run* (2026-06-06, reps = 1). Ela **não** estabelece **estabilidade temporal** — para isso é necessária ao menos uma segunda execução em data distinta (ver limitação #2). Portanto a limitação não está totalmente resolvida.

---

### 5. Reprodutibilidade pública parcial por design

A reprodução integral do experimento requer acesso ao dataset, prompts e verificador protegidos — que são segredo industrial. A reprodutibilidade pública é, portanto, parcialmente limitada por decisão deliberada. Ver [Declaração de reprodutibilidade](BEORYS_PCT_v0.2_REPRODUCIBILITY_STATEMENT.md).

---

### 6. Compliance estrutural ≠ veracidade factual

O benchmark mede **compliance estrutural de protocolo** contra verdade-base das tarefas — ou seja, se o modelo seguiu a estrutura exigida e não marcou como verificado o que não tinha evidência. Não mede a veracidade de afirmações factuais que o modelo possa inventar livremente dentro da estrutura correta. Detectar fabricação semântica de evidência é escopo para versões futuras.

---

### 7. Necessidade de auditoria independente futura

Para que os resultados ganhem status de evidência verificada externamente, é necessária auditoria independente por pesquisador ou entidade qualificada com acesso às evidências brutas sob NDA. Esta auditoria ainda não foi realizada na data de publicação deste documento.

---

### 8. Modelos em evolução

Os 5 modelos avaliados foram versões disponíveis em 2026-06-06. Modelos são continuamente atualizados por seus desenvolvedores; resultados para versões futuras dos mesmos modelos podem diferir.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
