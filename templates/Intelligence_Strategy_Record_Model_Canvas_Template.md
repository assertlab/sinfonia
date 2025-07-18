# Registro de Estratégia de Inteligência

## Instruções de Preenchimento

Use esta ficha para documentar a abordagem técnica escolhida para o núcleo de IA do projeto. Selecione a abordagem principal e preencha apenas as seções relevantes.

### 1. Objetivo da Inteligência

- **Instruções:** Descreva a tarefa específica que este componente de IA deve realizar.
- **Exemplo:** "Responder perguntas sobre agendamentos de consultas com base em uma base de conhecimento de documentos internos (FAQs, políticas)."

### 2. Abordagem Técnica Principal

- **Instruções:** Marque a estratégia dominante que será usada.
- **Exemplo:**
  - [ ] Treinamento de Modelo Customizado
  - [ ] Fine-Tuning de Modelo de Fundação
  - [X] RAG (Retrieval-Augmented Generation)
  - [ ] Engenharia de Prompt Avançada
  - [ ] Outra: ________________

### 3. Componentes Chave da Arquitetura

- **Instruções:** Com base na abordagem escolhida, descreva os principais "blocos de construção".
- **Exemplo (para RAG):**
  - **Fonte de Conhecimento:** "Documentos PDF e Word com políticas de agendamento e FAQs."
  - **Modelo de Embedding:** "text-embedding-004 da OpenAI"
  - **Vector Store:** "ChromaDB"
  - **Modelo de Geração:** "Google Gemini 1.5 Pro"

### 4. Fonte de Dados / Conhecimento

- **Instruções:** Descreva os dados que alimentarão o sistema.
- **Exemplo (para RAG):** "Corpus de 50 documentos internos da clínica, totalizando 300 páginas. Dados não estruturados (texto)."

### 5. Estratégia de Avaliação

- **Instruções:** Como saberemos que a inteligência está funcionando bem? Defina as métricas.
- **Exemplo (para RAG):**
  - **Métricas:** "Faithfulness (a resposta é baseada nos documentos?); Answer Relevancy (a resposta é relevante para a pergunta?); Avaliação qualitativa por 'Ana, a Recepcionista'."
  - **Ferramentas:** "Framework RAGAs, planilhas de avaliação manual."

### 6. Ferramentas e Time

- **Instruções:** Liste as principais ferramentas e os responsáveis.
- **Exemplo:**
  - **Ferramentas:** LangChain, ChromaDB, Google Cloud Platform.
  - **Time:** Engenheiro(a) de IA, Arquiteto(a) de Nuvem.
