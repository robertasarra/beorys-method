# BEORYS-PCT v0.2 — Declaração de Método

**Benchmark:** BEORYS Protocol Compliance Test (BEORYS-PCT) v0.2  
**Data de execução:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## 1. Identificação

| Campo | Valor |
|---|---|
| Nome do benchmark | BEORYS-PCT v0.2 |
| Versão | 0.2 |
| Data | 2026-06-06 |
| Modelos avaliados | 5 |
| Casos de avaliação | 100 |
| Categorias de tarefa | 7 |
| Execuções totais | 2.500 |
| Grupos de instrução | A, B, C, D, E |

---

## 2. Objetivo

Comparar a eficácia de diferentes métodos de instrução a LLMs para induzir compliance com o protocolo canônico BEORYS™, medida na primeira saída do modelo (sem repetição ou reformulação).

A única variável manipulada entre grupos é a **força e forma de imposição da instrução**. Tudo mais (conjunto de tarefas, categorias, modelos, parâmetros) permanece constante.

---

## 3. Grupos avaliados

| Grupo | Tipo de instrução |
|---|---|
| A | Prosa declarativa (regra em linguagem natural) |
| B | Checklist procedural (campos obrigatórios a preencher) |
| C | Auto-reflexão estruturada (revisão por ciclo interno) |
| D | Executor + validador LLM (separação de papéis, validador é modelo) |
| E | BEORYS™ (gate externo determinístico, fail-closed) |

---

## 4. Métricas

As métricas são aplicadas deterministicamente pelo mesmo verificador para todos os grupos. A lista de métricas é pública; os critérios operacionais de cada métrica são protegidos como segredo industrial.

Métricas publicadas:
- Protocol Compliance Rate
- Trigger Activation Rate
- Factual Assertion Detection Rate
- Evidence Attachment Rate
- Unauthorized Output Rate
- Self-Correction Failure Rate
- External Gate Block Rate (aplicável ao Grupo E)
- False Pass Rate (aplicável ao Grupo D)
- Recovery Rate (aplicável ao Grupo E)
- Auditability Score

---

## 5. Princípio de medição

- **Compliance de primeira tentativa:** a pontuação reflete o output não editado da primeira chamada ao modelo. Sem correções, sem reformulações.
- **Verificador determinístico único:** o mesmo verificador é aplicado a todos os grupos. Não há julgamento subjetivo na pontuação.
- **Regra de anticircularidade:** o verificador não é o mesmo modelo sendo avaliado. Verificadores são scripts determinísticos externos, não LLMs.

---

## 6. O que não é divulgado

Por decisão de proteção de segredo industrial, os seguintes elementos **não são publicados**:

- Prompts internos de cada grupo (completos ou parciais)
- Conjunto de casos individual (tarefas, verdades-base, saídas brutas)
- Critérios operacionais do verificador (thresholds, condições de bloqueio)
- Lógica de pipeline e orquestração
- Identidade individual dos modelos avaliados

---

## 7. Versão e relação com v0.1

O BEORYS-PCT v0.2 é uma versão ampliada e reestruturada do experimento interno v0.1. As diferenças de escopo entre versões não são publicadas. Os dados da v0.1 são evidência interna protegida.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
