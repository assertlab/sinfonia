# **Exemplo de Preenchimento: Registro de Estratégia de Inteligência (V1.0)**

- **1. Objetivo da Inteligência**

    - Responder perguntas complexas da recepcionista "Ana" sobre as políticas de agendamento da clínica, convênios aceitos por cada médico e regras para encaixes, utilizando a base de conhecimento interna de documentos da clínica.

- **2. Abordagem Técnica Principal**

    - [ ] Treinamento de Modelo Customizado
    - [ ] Fine-Tuning de Modelo de Fundação
    - [X] RAG (Retrieval-Augmented Generation)
    - [ ] Engenharia de Prompt Avançada
    - [ ] Outra: ________________

- **3. Componentes Chave da Arquitetura**

    - **Fonte de Conhecimento:** Manuais de políticas da clínica e tabelas de convênios por médico (em formato .docx e .pdf).
    - **Modelo de Embedding:** `text-embedding-004` (Google).
    - **Vector Store:** ChromaDB (rodando em um contêiner Docker).
    - **Modelo de Geração (LLM):** `Google Gemini 1.5 Pro` (via API).

- **4. Fonte de Dados / Conhecimento**

    - Corpus de aproximadamente 25 documentos internos da clínica, totalizando ~150 páginas. Os dados são não estruturados (texto em parágrafos) e semiestruturados (tabelas de convênios).

- **5. Estratégia de Avaliação**

    - **Métricas:**
        - `Answer Relevancy` (A resposta é relevante para a pergunta? Meta: 9/10).
        - `Faithfulness` (A resposta é 100% baseada nos documentos fornecidos? Meta: 10/10).
        - Avaliação qualitativa pela "Recepcionista Ana" em um conjunto de 50 perguntas-teste.
    - **Ferramentas:** Framework de avaliação RAGAs, planilhas de avaliação manual.

- **6. Ferramentas e Time**

    - **Ferramentas:** Python, LangChain, ChromaDB, Docker, Google Cloud Platform.
    - **Time:** Engenheiro(a) de IA (responsável pela pipeline RAG), Analista de Negócio (responsável por curar e validar os documentos fonte).
