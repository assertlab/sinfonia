# Exemplo de Preenchimento: Checklist de Lançamento

- **1. Objetivo e Escopo do Lançamento**
    
    - Lançar o MVP do assistente RAG para 20% dos recepcionistas (grupo piloto com 2 pessoas, incluindo a persona "Ana"). O objetivo é validar a usabilidade e a precisão das respostas em um ambiente real e controlado, antes da expansão para toda a equipe.
        
- **2. Estratégia de Lançamento**
    
    - **Abordagem:** Lançamento Canário (Canary Release), controlado por Feature Flag.
        
    - **Justificativa:** Liberar a funcionalidade apenas para o grupo piloto permite monitorar o impacto na infraestrutura e coletar feedback detalhado e de alta qualidade, sem afetar a operação principal da clínica.
        
- **3. Plano de Comunicação**
    
    - **Comunicação Interna:** E-mail para toda a equipe da clínica anunciando o início do piloto (Data: 20/07/2025). Sessão de treinamento prático de 1 hora com as 2 recepcionistas do grupo piloto (Data: 23/07/2025).
        
    - **Comunicação Externa:** Não se aplica para este lançamento piloto.
        
- **4. Plano de Contingência e Rollback**
    
    - **Gatilho de Rollback:** Se a taxa de erro da API do assistente exceder 5% na primeira hora, ou se o feedback do grupo piloto for majoritariamente negativo, indicando bloqueio na operação diária.
        
    - **Plano de Ação:** Desativar o feature flag do chatbot para o grupo piloto via painel de controle administrativo. O sistema retorna imediatamente à interface anterior. Tempo estimado para rollback: < 5 minutos.
        
- **5. Critérios de "Go/No-Go"**
    
    - `[X]` Todos os testes críticos do `Canvas de Testes e Validação` foram aprovados.
        
    - `[X]` A equipe de suporte e os engenheiros de plantão foram notificados e estão de prontidão para o dia do lançamento (Data: 25/07/2025).
        
    - `[X]` O plano de rollback (desativar o feature flag) foi testado com sucesso no ambiente de homologação.
        
    - **Go/No-Go Decisão Final (Data: 24/07/2025):** **[X] GO** / [ ] NO-GO
