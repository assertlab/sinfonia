# Painel de Feedback e Insights

## Instruções de Preenchimento
Use este painel para consolidar e analisar os feedbacks recebidos de múltiplas fontes. O objetivo é transformar dados brutos de feedback em insights acionáveis que informarão o próximo ciclo de planeamento do produto.

### 1. Objetivo do Ciclo de Feedback
- **Instruções**: Qual é a principal pergunta que queremos responder com o feedback deste período?
- **Exemplo**: "Entender por que a taxa de adoção do assistente está mais lenta do que o esperado entre os médicos mais seniores."

### 2. Fontes e Métodos de Coleta
- **Instruções**: Liste de onde e como o feedback foi recolhido neste ciclo.
- **Exemplo**:
  - **Fonte**: Médicos seniores, Logs de uso.
  - **Método**: Entrevistas individuais, análise de funil de uso no Datadog.

### 3. Principais Feedbacks Recebidos (Dados Brutos)
- **Instruções**: Liste os feedbacks mais recorrentes ou impactantes, agrupados por tema.
- **Exemplo**:
  - **Tema: Usabilidade**: "O chatbot exige muitos cliques para chegar à funcionalidade de resumo de histórico."
  - **Tema: Confiança**: "Não tenho a certeza se o resumo da IA é completo; prefiro ler o documento original."
  - **Tema: Desempenho**: "A geração do resumo demora mais de 10 segundos, o que é muito tempo durante uma consulta."

### 4. Insights Gerados (Síntese)
- **Instruções**: Transforme os feedbacks brutos em insights. Qual é a causa raiz ou a conclusão principal?
- **Exemplo**:
  - **Insight 1**: O fluxo de interação atual não está otimizado para a velocidade exigida no ambiente de uma consulta médica.
  - **Insight 2**: Existe uma barreira de confiança na precisão da IA que impede a adoção por utilizadores mais experientes.

### 5. Ações Recomendadas (Para o Backlog)
- **Instruções**: Sugira ações ou épicos de alto nível para abordar os insights. Estas são as recomendações que serão levadas para a reunião de planeamento de backlog/sprint.
- **Exemplo**:
  - **Ação Sugerida 1 (Epic)**: "Criar 'Atalhos de um clique' para as funcionalidades mais usadas (como 'Resumir Histórico') na interface principal."
  - **Ação Sugerida 2 (Spike/Investigação)**: "Investigar e prototipar uma funcionalidade de 'fontes citadas', onde o resumo da IA destaca as partes do texto original de onde extraiu a informação para aumentar a confiança."
