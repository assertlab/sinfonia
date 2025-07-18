# Checklist de Lançamento

## Instruções de Preenchimento
Use este checklist para garantir que todos os aspectos críticos do lançamento estejam planejados e alinhados. Ele serve como o documento final de "Go/No-Go" para a implantação.

### 1. Objetivo e Escopo do Lançamento
- **Instruções:** Descreva sucintamente o que será lançado nesta versão e qual o objetivo principal desta entrega.
- **Exemplo:** "Lançar o MVP do assistente RAG para 20% dos recepcionistas (grupo piloto) para validar a usabilidade e a precisão das respostas em um ambiente real."

### 2. Estratégia de Lançamento
- **Instruções:** Defina a abordagem do lançamento e justifique a escolha.
- **Exemplo:**
  - **Abordagem:** Lançamento Canário (Canary Release).
  - **Justificativa:** Liberar para um pequeno grupo de usuários permite monitorar o impacto real na infraestrutura e coletar feedback controlado antes de uma liberação em massa.

### 3. Plano de Comunicação
- **Instruções:** Detalhe quem precisa ser comunicado sobre o lançamento, quando e como.
- **Exemplo:**
  - **Comunicação Interna:** "E-mail para toda a clínica 1 semana antes. Reunião de treinamento com o grupo piloto de recepcionistas 2 dias antes."
  - **Comunicação Externa:** "N/A para este lançamento piloto."

### 4. Plano de Contingência e Rollback
- **Instruções:** Descreva o plano de emergência. O que faremos se algo crítico der errado durante ou logo após a implantação?
- **Exemplo:**
  - **Gatilho de Rollback:** "Se a taxa de erro da API do assistente exceder 5% na primeira hora."
  - **Plano de Ação:** "Desativar o feature flag do chatbot, retornando a interface ao seu estado anterior. A operação não é impactada."

### 5. Critérios de "Go/No-Go"
- **Instruções:** Liste as condições que DEVEM ser verdadeiras para que o lançamento seja autorizado.
- **Exemplo:**
  - [X] Todos os testes de aceitação críticos do `Canvas de Testes e Validação` foram aprovados.
  - [X] A equipe de suporte está treinada e de prontidão.
  - [X] O plano de rollback foi testado em ambiente de homologação.
  - [ ] **Go/No-Go Decisão Final:** [ ] GO / [ ] NO-GO
