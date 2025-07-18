
## **Exemplo 1: Diagrama de Contexto (Nível 1)**

- **Título**: "Diagrama de Contexto para o Assistente de Agendamento Inteligente"
    
- **Elementos e Interações**:
    
    - **Sistema Central**:
        
        - `Assistente de Agendamento Inteligente`: Sistema principal que automatiza e otimiza o agendamento de consultas.
            
    - **Atores (Usuários)**:
        
        - `Paciente`: Um indivíduo buscando marcar, remarcar ou cancelar uma consulta.
            
            - **Interação**: Solicita agendamentos e recebe confirmações via chat ou portal.
                
        - `Recepcionista (Ana)`: Funcionária da clínica que gerencia as agendas e lida com casos complexos.
            
            - **Interação**: Utiliza o assistente para consultar horários, gerenciar exceções e supervisionar o processo de agendamento automático.
                
    - **Atores (Sistemas Externos)**:
        
        - `Sistema de Prontuário Eletrônico (HIS)`: O sistema legado da clínica que armazena os dados dos pacientes.
            
            - **Interação**: O Assistente consulta o HIS para validar informações do paciente.
                
        - `Gateway de Email & SMS`: Serviço externo para envio de notificações.
            
            - **Interação**: O Assistente utiliza o gateway para enviar lembretes e confirmações de consulta aos pacientes.
                

---

## **Exemplo 2: Diagrama de Contêiner (Nível 2)**

- **Título**: "Diagrama de Contêiner para o Assistente de Agendamento Inteligente"
    
- **Elementos e Interações**:
    
    - **Contêiner 1: Aplicação Web (Frontend)**
        
        - **Descrição**: Interface de usuário (chatbot) onde pacientes e a recepcionista interagem com o sistema.
            
        - **Tecnologia**: React.js, WebSocket.
            
        - **Interação**: Envia requisições do usuário para a API de Agendamento.
            
    - **Contêiner 2: API de Agendamento (Backend)**
        
        - **Descrição**: Orquestra a lógica de negócio, processa as solicitações e se comunica com outros serviços.
            
        - **Tecnologia**: Python (FastAPI).
            
        - **Interação**: Recebe requisições do Frontend; consulta e atualiza o Banco de Dados; solicita análises do Serviço de IA; envia tarefas para a Fila de Notificações.
            
    - **Contêiner 3: Serviço de IA**
        
        - **Descrição**: Um microsserviço dedicado que encapsula os modelos de IA para recomendação e processamento de linguagem.
            
        - **Tecnologia**: Python, TensorFlow, LangChain.
            
        - **Interação**: Recebe solicitações da API de Agendamento para gerar recomendações de horários ou interpretar a intenção do usuário.
            
    - **Contêiner 4: Banco de Dados Principal**
        
        - **Descrição**: Armazena todas as informações sobre consultas, horários dos médicos e dados de pacientes (não sensíveis).
            
        - **Tecnologia**: PostgreSQL.
            
        - **Interação**: É lido e escrito pela API de Agendamento.
            
    - **Contêiner 5: Fila de Notificações**
        
        - **Descrição**: Gerencia o envio assíncrono de lembretes e confirmações para não bloquear a API principal.
            
        - **Tecnologia**: RabbitMQ.
            
        - **Interação**: Recebe mensagens da API de Agendamento para disparar notificações.
            

---

## **Exemplo 3: Diagrama de Componente (Nível 3)**

- **Título**: "Diagrama de Componentes para o **Serviço de IA**"
    
- **Elementos e Interações**:
    
    - **Componente 1: Controlador da API (API Controller)**
        
        - **Descrição**: Ponto de entrada do serviço. Expõe os endpoints (ex: `/recomendar_horario`) e valida as requisições recebidas da API de Agendamento.
            
        - **Tecnologia**: FastAPI.
            
        - **Interação**: Delega a lógica para os componentes de serviço apropriados.
            
    - **Componente 2: Motor de Recomendação**
        
        - **Descrição**: Componente principal que contém a lógica para analisar as agendas e encontrar os melhores horários.
            
        - **Tecnologia**: Lógica em Python com um modelo TensorFlow (.h5) carregado.
            
        - **Interação**: É chamado pelo Controlador; solicita dados históricos ao componente de Acesso a Dados.
            
    - **Componente 3: Gerador de Prompts**
        
        - **Descrição**: Constrói os prompts exatos a serem enviados para um LLM externo, com base nas Fichas de Prompt definidas.
            
        - **Tecnologia**: Módulo Python.
            
        - **Interação**: É usado pelo Controlador quando uma tarefa de Processamento de Linguagem Natural é necessária.
            
    - **Componente 4: Cliente do LLM**
        
        - **Descrição**: Encapsula a lógica de comunicação (chamadas HTTP, tratamento de erros, etc.) com uma API de IA externa (ex: Google Gemini API).
            
        - **Tecnologia**: Biblioteca de cliente da API (ex: `google-generativeai`).
            
        - **Interação**: Envia os prompts gerados e retorna a resposta do LLM.
            
    - **Componente 5: Acesso a Dados (Data Access)**
        
        - **Descrição**: Responsável por se comunicar com o Banco de Dados Principal para buscar os dados necessários para os modelos.
            
        - **Tecnologia**: SQLAlchemy.
            
        - **Interação**: É utilizado pelo Motor de Recomendação para obter dados de agendamentos passados.
