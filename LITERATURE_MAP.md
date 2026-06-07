# LITERATURE_MAP — Mapa Afirmação → Fonte

**BEORYS™** | Curadoria: 2026-06-06 | Titular: Roberta Sarra España

Este mapa conecta cada afirmação técnica do BEORYS™ às fontes que a sustentam. Distingue força de evidência e anota quando uma afirmação depende de preprints.

---

## Mapa principal

| Afirmação técnica | Fontes que sustentam | Força da evidência | Observação |
|---|---|---|---|
| Regras declarativas em prosa são sistematicamente ignoradas sob geração fluente conforme o output cresce | IFEval, FollowBench, DeCRIM, InFoBench, FireBench | **Forte** | Múltiplas fontes convergentes; IFEval, FollowBench e DeCRIM são peer-reviewed; FireBench é preprint |
| Modelos de ponta violam pelo menos uma restrição em >21% das instruções reais multi-restrição | DeCRIM | **Forte** | Fonte peer-reviewed com medição direta sobre GPT-4 |
| Instrução procedimental/checklist supera prosa declarativa em compliance, mas sem bloqueio externo ainda é soft constraint | DeCRIM, InFoBench, FASTRIC | **Moderada** | Melhora documentada; limite sem gate externo inferido; FASTRIC é preprint |
| Auto-correção interna do modelo é insuficiente como mecanismo primário de garantia sem feedback externo forte | Kamoi et al. (TACL), CRITIC, Self-Refine | **Forte** | TACL é peer-reviewed; explicita que sem sinal externo o modelo corrige o que estava certo |
| Sem fine-tuning, ciclos de revisão (reflexão verbal, memória episódica) produzem ganhos mas são insuficientes para garantia de protocolo | Reflexion, Self-Refine | **Moderada** | Confirmam viabilidade de refino iterativo; não confirmam falha-zero de protocolo |
| Separar quem gera de quem valida eleva qualidade além do que o gerador sozinho alcança | StrongVerifiers, CRITIC, NeMo, BEAVER | **Forte** para o princípio; **moderada** para a forma específica do gate BEORYS™ | StrongVerifiers e NeMo são peer-reviewed; BEAVER é preprint diretamente alinhado |
| Planejar verificação antes de afirmar (gate pré-bloco) reduz alucinação | CoVe | **Forte** | Fonte peer-reviewed; embasa diretamente o princípio de gate pré-bloco do BEORYS™ |
| Verificação por critérios atômicos sim/não é mais confiável que avaliação global | InFoBench (DRFR), FollowBench | **Forte** | Ambas peer-reviewed; DRFR decompõe em 2.250 critérios avaliáveis |
| Constrained decoding / hard constraint de formato é superior a instrução para outputs estruturados consumidos por máquina | JSONSchemaBench | **Moderada** | Preprint; confirma o princípio; não substitui gate semântico |
| Gate fail-closed melhora auditabilidade vs. outros métodos testados | Benchmark BEORYS-PCT v0.2 (interno/agregado) | **Interna** | Evidência própria da titular; requer auditoria independente futura para validação externa |
| Aderência inconsistente a instruções custom é problema documentado em ambiente enterprise/API | DeCRIM, FireBench, InstructionGap | **Moderada** | DeCRIM peer-reviewed; FireBench e InstructionGap são preprints |

---

## Legenda de força de evidência

| Nível | Descrição |
|---|---|
| **Forte** | Sustentada por ≥1 fonte peer-reviewed com medição direta do fenômeno afirmado |
| **Moderada** | Sustentada por peer-reviewed adjacente ou por múltiplos preprints convergentes; não medição direta |
| **Interna** | Sustentada apenas pelo benchmark interno BEORYS-PCT; requer auditoria externa futura |

---

## Afirmações sem suporte acadêmico publicado (internas ao método)

As seguintes afirmações são parte do método BEORYS™ e não têm equivalente direto na literatura pública verificada. São apresentadas como tese do método, não como resultado acadêmico:

- A formulação exata "A fluência pode redigir; não pode autorizar" — princípio original da titular
- Os critérios operacionais específicos dos gates BEORYS™
- A arquitetura de separação executor/validador na forma específica implementada

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
