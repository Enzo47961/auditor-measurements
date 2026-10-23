# auditor-measurements

Repositório **só de medições** do [auditor de integridade de provas Lean 4](https://github.com/Enzo47961/auditor), Fase 1.

> **Declaração obrigatória (L-26): `classification_review_status: author-self-review`.** A classificação dos comandos do Mathlib usada aqui (`.auditor/classification.toml`) foi elaborada e revisada pelo mesmo autor; não houve revisão independente. Nenhum número produzido aqui é alegação de cobertura do Mathlib a terceiros sem essa qualificação.

- **Conteúdo:** só workflows e a configuração do auditor para o Mathlib (`.auditor/`). Cada workflow baixa o Mathlib oficial (`leanprover-community/mathlib4`) **exatamente no commit fixado `e1b2403b`**, sobrepõe o `.auditor/` e confere o commit. Nenhum `.lean` do Mathlib é alterado ou versionado aqui.
- **Workflows** (todos só por disparo manual e só leitura; os resultados saem como artefato):

  | Workflow | O que faz |
  |---|---|
  | `auditor-mutation` | testes de mutação do auditor, nos grupos pedidos |
  | `auditor-prep` | allow-list do Mathlib, `gen_tcb_roots --check` e teste de fumaça |
  | `auditor-measure` | medições P0-1 e P0-2 |
  | `auditor-benchmark` | benchmark da sub-fase 1b |

  Nenhum deles commita, comenta ou abre PR.
- **Origem:** separado do fork de medição (`Enzo47961/mathlib4`) depois que o GitHub suspendeu os workflows do fork por uso intenso, em 2026-10-23. O fork continua com os PRs de medição da camada 2 e com os workflows de PR.
