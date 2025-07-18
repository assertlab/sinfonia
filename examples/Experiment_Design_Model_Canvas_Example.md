# **Exemplo de Preenchimento: Canvas de Desenho de Experimento (Versão 2.0)**

_Este exemplo foi adaptado para a nova estrutura focada em hipóteses e aprendizado._

- **1. Ideia a Ser Validada:**

    - Utilizar um assistente de IA para automação do agendamento de consultas.

- **2. Hipótese Principal:**

    - Acreditamos que **implementar um assistente de IA para a recepcionista Ana** resultará em **uma redução drástica no tempo de agendamento**. Saberemos que isso é verdade quando
  
        **o tempo médio para marcar uma consulta cair 50% durante os testes**2.
  
- **3. Desenho do Experimento (MVP):**

    - Um protótipo de chatbot "Wizard of Oz", onde um membro da equipe responde às perguntas dos usuários seguindo um script, simulando a IA. O objetivo é validar o fluxo da conversa e a aceitação da persona ("Ana"), utilizando dados históricos de agendamento 3 para as respostas, sem construir o modelo de IA ainda.

- **4. Métricas-Chave de Aprendizagem:**

    - Tempo médio de espera para marcação de consultas.
    - Taxa de sucesso (percentual de usuários que conseguem agendar sem precisar de ajuda extra).
    - Feedback qualitativo da recepcionista "Ana" sobre a facilidade e clareza do fluxo.

- **5. Critérios de Sucesso (Para "Pivotar ou Perseverar"):**

    - Se o tempo médio de agendamento for reduzido em pelo menos 40% (próximo da nossa meta de 50%) e o feedback qualitativo da "Ana" for positivo, a hipótese será considerada validada. Vamos **perseverar** e iniciar o desenvolvimento do modelo de IA real. Caso contrário, vamos **pivotar** e testar um novo fluxo de conversação ou uma nova abordagem.
