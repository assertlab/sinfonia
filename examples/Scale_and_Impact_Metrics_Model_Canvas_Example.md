# Exemplo de Preenchimento: Canvas de Métricas de Escala e Impacto

- **1. Objetivo do Monitoramento**

    - Monitorar o impacto do assistente na eficiência da equipe de recepção (grupo piloto) e garantir a qualidade técnica da solução.

- **2. Métricas de Uso**

    - **Número de interações diárias:** 50 (crescendo 10% por semana).
    - **Usuários ativos por semana:** 2 (100% do grupo piloto).
    - **Taxa de adoção:** 100% (o grupo piloto não utiliza mais o método antigo para estas tarefas).

- **3. Métricas de Desempenho**

    - **Tempo médio de resposta:** 1.8 segundos.
    - **Taxa de erro (respostas "não sei" ou incorretas):** 4%.
    - **Latência da busca no Vector Store (p95):** 1.2 segundos.

- **4. Métricas de Impacto no Negócio**

    - **Tempo economizado pela equipe:** Estimado em 30 minutos/dia por recepcionista.
    - **Redução de erros de informação sobre convênios:** 100% (zero erros reportados pelo piloto).

- **5. Métricas de Satisfação do Usuário**

    - **CSAT da recepcionista "Ana":** 9.5/10.
    - **Feedback qualitativo:** "É muito mais rápido e confiável para dúvidas complexas sobre convênios."

- **6. Ferramentas de Monitoramento**

    - **Desempenho e Uso:** Datadog, Logs internos da aplicação.
    - **Satisfação:** Entrevistas semanais com o grupo piloto.

- **7. Benchmarks**

    - **Tempo médio de resposta ideal:** ≤ 2 segundos.
    - **Taxa de erro ideal:** < 5%.

- **8. Acompanhamento de Tendências**

    - **Relatórios semanais de uso e desempenho.**
    - **Análise:** O crescimento de 10% por semana no uso indica que um lançamento para toda a clínica (10 recepcionistas) excederá a capacidade da infraestrutura atual em aproximadamente 2 meses.

- **9. Ações Baseadas nas Métricas**

    - **Ação Imediata:** Iniciar o planejamento de escalabilidade para o lançamento completo.
    - **Ação Contínua:** Revisar os 4% de interações com erro para otimizar os documentos da base de conhecimento.

- **10. Relatórios e Compartilhamento**

    - Dashboard no Datadog compartilhado com a equipe técnica.
    - Relatório mensal de impacto de negócio enviado para a diretoria da clínica.
