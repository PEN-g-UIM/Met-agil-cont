# Atividade Prática: Kanban para Produto Regulamentado

**Disciplina:** Metodologias Ágeis
**Cenário:** Portal MedDados (Caso C: produto regulamentado)
**Abordagem:** Kanban com práticas de XP
**Formato:** grupo de 5 pessoas, apresentação de até 4 minutos

---

## Passo 1: Diagnóstico do cenário

| Aspecto | Situação |
|---|---|
| **Produto e usuários** | Portal web de clínicas com dados sensíveis de saúde e auditoria obrigatória. Usuários: pacientes, médicos e atendimento. |
| **Demanda** | Contínua e variada (funcionalidades, correções, ajustes legais, incidentes), com alguns prazos fixos. |
| **Equipe** | 5 pessoas, pouca prática técnica, conhecimento concentrado em poucos. |
| **Tecnologia** | Sistema legado, poucos testes automatizados, deploy manual. |
| **Organização e restrições** | Toda mudança exige validação de compliance, com evidência documental e alto impacto em caso de falha. |
| **Principais dores e riscos** | Trabalho travado na validação, defeitos descobertos tarde, documentação feita no fim e urgências sem critério. |

---

## Passo 2: Proposta

- **Abordagem principal:** Kanban, com práticas de XP.
- **Objetivo da escolha:** dar visibilidade ao fluxo (principalmente à fila de validação) e melhorar a qualidade sem eliminar documentação e controles.
- **Práticas adotadas:**
  - Quadro visual
  - Limites de WIP
  - Classes de serviço (Urgente, Prazo fixo, Padrão)
  - DoD com requisitos regulatórios
  - TDD e integração contínua nos pontos críticos
  - Programação em pares em partes sensíveis
- **Não são prioridade agora:** Sprints com escopo fechado e refatoração em larga escala do legado.
- **Fluxo:**
  `Backlog` → `Em desenvolvimento` → `Revisão técnica` → `Validação de compliance` → `Pronto para implantar` → `Concluído`
- **Responsabilidades e políticas:**
  - Só entra em revisão com testes passando.
  - Só conclui com a DoD cumprida.
  - Máximo de 1 urgente por vez.
  - Compliance com horários fixos de validação.
- **Feedback esperado:**
  - Reunião diária
  - Reposição semanal do backlog
  - Revisão quinzenal do fluxo

---

## Passo 3: Riscos e evidências

| Risco | Impacto | Mitigação |
|---|---|---|
| Compliance vira gargalo | Atrasos e prazos legais perdidos | Janelas fixas de validação e compliance envolvido desde os critérios de aceitação |
| Tudo vira urgente | Fluxo destruído | Limite de 1 urgente com justificativa |
| WIP e DoD ignorados | Qualidade e auditoria comprometidas | Acordo coletivo e revisão quinzenal das políticas |

**3 evidências para acompanhar a adaptação:**

1. Tempo de ciclo (e tempo parado na validação)
2. Itens bloqueados
3. Frequência de defeitos após a validação

---

## Passo 4: Apresentação (até 4 minutos)


| Pessoa | Tema | Fala |
|---|---|---|
| 1 | Contexto | Portal MedDados, dados sensíveis, auditoria obrigatória. |
| 2 | Problema prioritário | O trabalho trava na validação e na documentação, e ninguém enxerga isso. |
| 3 | Abordagem e práticas | Kanban + XP, com quadro, WIP, classes de serviço, DoD, TDD e CI. |
| 4 | Justificativa | A demanda é contínua e variada, então Sprints fechadas não cabem. Agilidade não elimina controles, ela os integra ao fluxo. |
| 5 | Um risco e uma evidência | Risco: tudo virar urgente, mitigado com limite de 1 urgente. Evidência: tempo parado na validação de compliance. |


