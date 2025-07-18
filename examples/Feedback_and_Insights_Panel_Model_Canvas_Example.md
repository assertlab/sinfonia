# Exemplo de Preenchimento: Painel de Feedback e Insights

- **1. Objetivo do Ciclo de Feedback**

    - Entender por que a pontuação de satisfação (CSAT) do assistente está mais baixa entre os recepcionistas mais experientes (7/10) em comparação com os mais novos (9.5/10) e identificar oportunidades de melhoria para aumentar a confiança no sistema.

- **2. Fontes e Métodos de Coleta**

    - **Fonte:** Recepcionistas seniores (3 pessoas com mais de 5 anos de casa).
    - **Método:** Entrevistas individuais de 30 minutos com cada um.
    - **Fonte:** Logs de interação do assistente.
    - **Método:** Análise das conversas que terminaram com uma baixa avaliação ou que foram escaladas para um supervisor humano.

- **3. Principais Feedbacks Recebidos (Dados Brutos)**

    - **Tema: Confiança e Transparência:** "A resposta do assistente é muito direta. Eu não sei _de onde_ ele tirou aquela informação. Com o sistema antigo, eu mesmo via o documento de convênios para ter certeza."
    - **Tema: Casos de Borda (Complexos):** "Para agendamentos complexos, como 'paciente X precisa de 2 exames no mesmo dia com o Dr. Y', o assistente se perde. Eu acabo fazendo manualmente, o que leva mais tempo."
    - **Tema: Velocidade vs. Detalhe:** "Ele é rápido para perguntas simples, mas para casos em que preciso de mais detalhes, sinto que 'luto' com o bot para conseguir a informação, tendo que fazer várias perguntas."

- **4. Insights Gerados (Síntese)**

    - **Insight 1:** A falta de transparência sobre a fonte da informação gera desconfiança nos utilizadores experientes, que estão acostumados a verificar os dados originais e precisam de um alto grau de certeza.
    - **Insight 2:** O assistente foi otimizado para tarefas de alta frequência (perguntas e agendamentos simples), mas ainda não lida bem com fluxos de trabalho que exigem a combinação de múltiplas restrições.

- **5. Ações Recomendadas (Para o Backlog)**

    - **Ação Sugerida 1 (Epic):** "Implementar 'Rastreabilidade da Resposta'". Investigar e prototipar uma funcionalidade onde o assistente, ao fornecer uma resposta, também oferece um link ou referência para a seção do documento de onde a informação foi extraída.
    - **Ação Sugerida 2 (Spike/Investigação):** "Mapear os 5 tipos de 'agendamentos complexos' mais comuns. Criar `Fichas de Prompt` específicas para esses cenários e avaliar a viabilidade de um fluxo de conversa multi-etapas para lidar com eles."
