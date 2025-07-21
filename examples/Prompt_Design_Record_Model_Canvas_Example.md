# Registro de Design de Prompt: RESUMO-HISTORICO-PACIENTE-01

## 1. Metadados

- **Propósito:** Resumir o histórico médico de um paciente em um parágrafo conciso para que o médico possa se preparar rapidamente antes de iniciar a consulta.
- **Modelo(s) Alvo:** Google Gemini 1.5 Pro (otimizado para resumos de texto longo).
- **Versão do Registro:** 1.0

## 2. Estrutura do Prompt

- **Contexto de Entrada Necessário:** Texto completo do histórico do paciente (string); Nome do médico (string); Nome do paciente (string).
- **Template do Prompt (com variáveis):**
  "Você é um assistente médico perito. Para o Dr. `{nome_medico}`, resuma o seguinte histórico do paciente `{nome_paciente}`. O resumo deve ser objetivo, ter no máximo 100 palavras e focar nos últimos diagnósticos e medicações ativas. Histórico: ```{texto_historico}```"

## 3. Estrutura da Resposta

- **Intenção da Resposta:** Um parágrafo único de texto em português, escrito em linguagem técnica clara para um profissional de saúde, omitindo informações redundantes.
- **Exemplo de Saída Ideal:**
  "Paciente Maria Silva, 45 anos. Diagnósticos relevantes: hipertensão controlada e diabetes tipo 2. Medicação ativa: Losartana 50mg e Metformina 850mg. Última consulta em 15/06/2025 mostrou bom controle glicêmico e ausência de novas queixas."

## 4. Teste e Qualidade

- **Critérios de Aceite / Métricas de Qualidade:**
  - 1. O resumo DEVE ter menos de 120 palavras.
  - 2. DEVE mencionar o(s) diagnóstico(s) principal(is) e a medicação ativa.
  - 3. NÃO DEVE incluir informações pessoais de contato (endereço, telefone) para conformidade com a LGPD.
  - 4. A linguagem DEVE ser objetiva e factual.
- **Parâmetros Recomendados (Opcional):**
  - "Temperatura: 0.2 (para garantir alta fidelidade ao texto original e pouca criatividade)."

## 5. Notas Adicionais
- **Instruções:** O prompt pode ter dificuldade com abreviações médicas muito antigas ou caligrafia digitalizada. Recomenda-se testar com exemplos de dados de baixa qualidade.
