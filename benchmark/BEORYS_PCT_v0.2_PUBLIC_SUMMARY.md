# BEORYS-PCT v0.2 — Sumário Público

**Benchmark:** BEORYS Protocol Compliance Test v0.2  
**Data:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## O que foi testado

Quando instruímos um modelo de linguagem a seguir um protocolo, qual forma de instrução produz maior compliance — e, especificamente, maior ativação de verificação antes de afirmar?

O BEORYS-PCT v0.2 compara cinco abordagens (grupos A a E) em 100 casos, 7 categorias de tarefa, com 5 modelos, totalizando 2.500 execuções. A única variável entre grupos é a forma e força da instrução.

---

## O que os resultados mostram

O resultado mais importante não é a taxa geral de compliance (que permanece alta em todos os grupos), mas a **taxa de ativação de verificação** — o quanto cada método consegue fazer o modelo realmente verificar antes de afirmar.

| Grupo | Método | Trigger Activation Rate |
|---|---|---:|
| A | Prosa declarativa | 2% |
| B | Checklist procedural | 23% |
| C | Auto-reflexão estruturada | 23% |
| D | Executor + validador LLM | 2% |
| **E** | **BEORYS™ (gate externo fail-closed)** | **93%** |

Regras em prosa e separação executor/validador-LLM ativam verificação em apenas 2% dos casos. Checklist e auto-reflexão chegam a 23%. O gate externo determinístico do Grupo E ativa verificação em 93% dos casos — enquanto rejeita silenciosamente 0% (cada bloqueio é rastreável: External Gate Block Rate = 6%).

---

## O que isso significa

A fluência do modelo não é o problema — é o mecanismo de ativação da verificação. Dizer "verifique antes de afirmar" em prosa não funciona: o modelo já está gerando quando chega ao momento de verificar, e a verificação é ignorada. Apenas um mecanismo externo ao fluxo de geração consegue ativar a verificação de forma consistente.

Isso é o que o princípio BEORYS™ codifica:

> **"A fluência pode redigir; não pode autorizar."**

---

## O que este sumário não revela

- Os prompts internos de cada grupo
- Os 100 casos de avaliação
- A identidade dos 5 modelos
- Os critérios operacionais do verificador
- Qualquer dado individual (por caso, por modelo, por output)

Esses elementos são segredo industrial — ver [TRADE_SECRET.md](../legal/TRADE_SECRET.md).

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*  
*Citação autorizada com atribuição: Roberta Sarra España, BEORYS-PCT v0.2, 2026.*
