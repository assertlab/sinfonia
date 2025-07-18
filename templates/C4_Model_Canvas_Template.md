# Nível de Contexto

**Descrição**: Mostra os atores externos (usuários, sistemas, dispositivos) e sua interação com o sistema de IA. Ideal para comunicar o propósito geral e o papel do assistente.

## Estrutura do Template:
1. **Título**: "Diagrama de Contexto para [Nome do Assistente]"
2. **Elementos**:
   - Retângulo central representando o sistema principal (Assistente Inteligente).
   - Retângulos menores representando os atores externos (usuários, sistemas).
   - Linhas conectando os atores ao sistema, com anotações explicando o tipo de interação.
3. **Legenda** (opcional): Para indicar cores ou símbolos que diferenciam tipos de atores ou interações.

## Exemplo Prático:
- **Assistente Inteligente**:
  - **Usuários**: Pacientes, Recepcionistas.
  - **Sistemas**: CRM, Banco de Dados de Consultas.
  - **Interações**:
    - Paciente → Assistente: "Quero agendar uma consulta."
    - Assistente → CRM: "Buscar dados do paciente."
    - Assistente → Banco de Dados: "Atualizar consulta agendada."

# Nível de Contêiner

**Descrição**: Detalha os componentes principais do sistema, como serviços de backend, bancos de dados, interfaces de usuário e APIs.

## Estrutura do Template:
1. **Título**: "Diagrama de Contêiner para [Nome do Assistente]"
2. **Elementos**:
   - Retângulos representando contêineres (Frontend, Backend, Banco de Dados, Serviços de IA).
   - Linhas indicando interações entre contêineres.
   - Anotações nos contêineres com tecnologias usadas.
3. **Legenda** (opcional): Diferencia tipos de contêineres (por exemplo, armazenamento, lógica de negócios, interface).

## Exemplo Prático:
- **Frontend (Chatbot)**:
  - Tecnologia: React + WebSocket.
  - Função: Interagir com os usuários.
- **Serviço de IA**:
  - Tecnologia: FastAPI + TensorFlow.
  - Função: Gerar recomendações e processar consultas.
- **Banco de Dados**:
  - Tecnologia: PostgreSQL.
  - Função: Armazenar consultas e informações de pacientes.

# Nível de Componente

**Descrição**: Detalha os componentes internos de um contêiner, mostrando como as funcionalidades são divididas e interligadas.

## Estrutura do Template:
1. **Título**: "Diagrama de Componentes para [Nome do Contêiner]"
2. **Elementos**:
   - Retângulos pequenos representando os componentes.
   - Linhas indicando fluxos de dados ou dependências entre componentes.
   - Anotações explicando funções e tecnologias específicas.
3. **Legenda**: Explica cores ou símbolos usados para diferenciar tipos de componentes (ex.: processamento, dados, APIs).

## Exemplo Prático:
- **Serviço de IA**:
  - **Gerador de Prompts**:
    - Função: Criar mensagens baseadas nas intenções do usuário.
    - Tecnologia: LangChain.
  - **Recomendador de Horários**:
    - Função: Sugerir horários ideais.
    - Tecnologia: TensorFlow.
  - **Validador de Consultas**:
    - Função: Validar horários disponíveis.
    - Tecnologia: Python.
