# Fundamentação Acadêmica — BEORYS™

**Tema:** Como impor que um LLM respeite protocolo durante geração fluente  
**Data da curadoria:** 2026-06-06  
**Titular:** Roberta Sarra España

---

## 1. Tese

> **A confiabilidade não emerge da fluência.**

Instruções declarativas em linguagem natural — "nunca afirme um fato sem verificar", "não encerre sem completar o sumário" — são sistematicamente ignoradas conforme a geração avança. A explicação técnica: a geração fluente é um processo de predição de tokens que privilegia coerência local; restrições globais declaradas no prompt competem com essa dinâmica e perdem progressivamente.

A consequência prática: qualquer sistema que dependa de compliance via prosa está construído sobre um mecanismo intrinsecamente fraco. A solução estrutural é **separar quem gera de quem autoriza**, delegando a autorização a um verificador externo, determinístico e de falha-fechada.

---

## 2. Literatura principal

### 2.1 Fontes revisadas por pares (peer-reviewed)

| Referência | Venue | Contribuição relevante | DOI / URL |
|---|---|---|---|
| IFEval — Zhou et al. (2023) | arXiv (referência para benchmarks de IF) | Define 25 tipos de instrução verificável programaticamente; documenta falha de modelos conforme output cresce | `10.48550/arXiv.2311.07911` |
| Self-Refine — Madaan et al. (2023) | NeurIPS 2023 | Mostra que refinamento iterativo por crítica é viável sem fine-tuning; fundamento para ciclos de revisão | `10.48550/arXiv.2303.17651` |
| Reflexion — Shinn et al. (2023) | NeurIPS 2023 | Agente Actor–Evaluator–Reflector sem atualização de pesos; performance aumenta via feedback linguístico | `10.48550/arXiv.2303.11366` |
| Chain-of-Verification (CoVe) — Dhuliawala et al. (2023) | arXiv / ACL 2024 | Planejar verificação ANTES do output final reduz alucinação; embasa gate pré-bloco | `10.48550/arXiv.2309.11495` |
| CRITIC — Gou et al. (2023) | ICLR 2024 | Auto-correção via ferramenta externa; análogo de trava física por script determinístico | `10.48550/arXiv.2305.11738` |
| "When Can LLMs Actually Correct Their Own Mistakes?" — Kamoi et al. (2024) | TACL 2024 | **Evidência contra** auto-correção interna sem feedback externo forte; sem sinal externo o modelo "corrige" o que estava certo | `10.1162/tacl_a_00713` |
| DeCRIM — Puttaparthi et al. (2024) | EMNLP Findings 2024 | GPT-4 viola ≥1 restrição em >21% das instruções reais multi-restrição; decompor + criticar + refinar melhora compliance | `10.18653/v1/2024.findings-emnlp.458` |
| InFoBench / DRFR — Qin et al. (2024) | ACL Findings 2024 | Decomposição de instruções em 2.250 critérios atômicos sim/não; avaliação granular de compliance | `10.18653/v1/2024.findings-acl.772` |
| FollowBench — Jiang et al. (2024) | ACL 2024 | Restrições finas multi-nível; compliance cai com profundidade de restrições | `10.18653/v1/2024.acl-long.257` |
| Strong Verifiers — Zheng et al. (2024) | ACL Findings 2024 | Separar gerador de verificador forte eleva qualidade além do que o gerador sozinho alcança | `10.18653/v1/2024.findings-acl.924` |
| NeMo Guardrails — Rebedea et al. (2023) | EMNLP 2023 | Trilhos externos programáveis (Colang) sobre LLMs; arquitetura de controle externo | `arXiv:2310.10501` |

### 2.2 Preprints verificados em arXiv (não revisados por pares; usados como corroboração)

> **Regra de uso:** preprints recentes não podem ser a base única de afirmação forte. São usados aqui como corroboração de afirmações já sustentadas por fontes peer-reviewed.

| Referência | Data arXiv | Contribuição relevante | ID |
|---|---|---|---|
| JSONSchemaBench — Geng et al. (2025) | Jan 2025 | Constrained decoding / saída estruturada; hard constraint de formato para outputs consumidos por máquina | `arXiv:2501.10868` |
| BEAVER (2025) | Dez 2025 | "Efficient Deterministic LLM Verifier" — separação executor/validador; diretamente relevante para a arquitetura BEORYS™ | `arXiv:2512.05439` |
| Instruction Gap (2026) | Jan 2026 | Aderência inconsistente a instruções custom em ambiente enterprise/API | `arXiv:2601.03269` |
| FASTRIC (2025) | Dez 2025 | Linguagem de especificação de prompt para interações verificáveis | `arXiv:2512.18940` |
| MOSAIC (2026) | Jan 2026 | Avaliação granular e modular de compliance de instrução | `arXiv:2601.18554` |
| FireBench — Fireworks AI (2026) | Mar 2026 | Instruction-following em apps enterprise/API-driven; violações de formato quebram pipelines | `arXiv:2603.04857` |

---

## 3. Ligação entre literatura e hipótese BEORYS™

| Afirmação BEORYS™ | Evidência acadêmica | Força |
|---|---|---|
| Regras declarativas em prosa são sistematicamente ignoradas sob geração fluente | IFEval, FollowBench, DeCRIM (>21% de violação em instrução real), InFoBench | **Forte** — múltiplas fontes peer-reviewed convergentes |
| Instrução procedimental (checklist) supera prosa, mas sem bloqueio ainda é soft constraint | DeCRIM, InFoBench, FASTRIC | **Moderada** — melhora documentada; limite sem gate externo confirmado |
| Auto-correção interna do modelo é insuficiente como mecanismo primário sem feedback externo forte | Kamoi et al. (TACL), CRITIC, Self-Refine | **Forte** — evidência de peer-reviewed explicitamente contra dependência de introspecção interna |
| Verificador externo determinístico reduz dependência da fluência e eleva auditabilidade | CRITIC, NeMo Guardrails, Strong Verifiers, BEAVER (preprint) | **Forte** para o princípio; **moderada** para a forma específica do gate BEORYS™ |
| Planejar verificação antes de afirmar reduz alucinação | CoVe | **Forte** para o princípio de gate pré-bloco |
| Gate fail-closed melhora auditabilidade vs. outros métodos | Benchmark BEORYS-PCT v0.2 (interno/agregado) | **Interna** — requer auditoria independente futura para validação externa |

---

## 4. Limites da evidência

1. **Generalização restrita:** os benchmarks acadêmicos medem tipos específicos de instrução em condições controladas. Resultados não generalizam automaticamente para todos os domínios de aplicação.

2. **Evolução dos modelos:** os modelos avaliados na literatura de 2023–2024 diferem dos modelos disponíveis em 2026. Compliance pode melhorar com novos modelos, mas o problema estrutural (prosa vs. gate) persiste.

3. **Auto-correção parcialmente útil:** Self-Refine e Reflexion mostram que ciclos de revisão ajudam. A afirmação do BEORYS™ não é que auto-correção é inútil, mas que é **insuficiente como mecanismo primário de garantia**.

4. **Benchmark interno:** o BEORYS-PCT v0.2 mede compliance estrutural de protocolo contra verdade-base das tarefas — não veracidade factual de evidências fabricadas livremente. Resultados não implicam prova universal.

5. **Preprints recentes:** fontes de 2025–2026 são preprints não revisados por pares. São usados como corroboração, nunca como base única de afirmação forte.

---

## 5. Nota metodológica sobre a curadoria

Os relatórios que embasaram esta síntese foram gerados por LLMs — exatamente o comportamento que o BEORYS™ desconfia. Portanto nenhuma citação entrou aqui sem verificação do DOI ou ID arXiv na fonte primária determinística. Todas as referências listadas foram confirmadas por acesso direto ao identificador canônico. Esta auto-aplicação do princípio BEORYS™ à própria pesquisa é documentada como meta-lição metodológica.

---

*Todos os direitos reservados. BEORYS™ é marca de Roberta Sarra España.*
