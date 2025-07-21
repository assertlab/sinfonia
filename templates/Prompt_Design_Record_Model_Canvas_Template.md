# Registro de Design de Prompt: \[ID ou Nome Curto do Prompt\]

- **Exemplo de ID:** `RESUMO-HISTORICO-PACIENTE-01`

## 1. Metadados

- **Propósito:** Descreva o objetivo de negócio deste prompt. O que ele deve realizar?
  - *Exemplo:* "Resumir o histórico médico de um paciente em um parágrafo conciso para o médico."
- **Modelo(s) Alvo:** Especifique se o prompt foi otimizado para um modelo específico e qual.
  - *Exemplo:* "Qualquer (genérico)", "OpenAI GPT-4", "Google Gemini 1.5 Pro".
- **Versão do Registro:**
  - *Exemplo:* "1.0"

## 2. Estrutura do Prompt

- **Contexto de Entrada Necessário:** Que informações devem ser fornecidas ao prompt para que ele funcione?
  - *Exemplo:* "Texto completo do histórico do paciente; Nome do médico solicitante."
- **Template do Prompt (com variáveis):** O texto exato do prompt, usando `{chaves}` para indicar as variáveis que serão injetadas.
  - *Exemplo:* "Você é um assistente médico. Resuma o seguinte histórico do paciente `{nome_paciente}` para o Dr. `{nome_medico}`. O resumo deve ser objetivo, ter no máximo 100 palavras e focar nos últimos diagnósticos e medicações ativas. Histórico: `{texto_historico}`"

## 3. Estrutura da Resposta

- **Intenção da Resposta:** Qual é o formato e a intenção da saída? É uma lista, um parágrafo, um JSON?
  - *Exemplo:* "Um parágrafo único de texto em português, escrito em linguagem clara e objetiva, sem jargões excessivos."
- **Exemplo de Saída Ideal:** Um exemplo concreto de uma resposta de alta qualidade.
  - *Exemplo:* "Paciente Maria Silva, 45 anos. Diagnósticos recentes incluem hipertensão controlada e diabetes tipo 2. Medicação ativa: Losartana 50mg e Metformina 850mg. Última consulta em 15/06/2025 mostrou bom controle glicêmico."

## 4. Teste e Qualidade

- **Critérios de Aceite / Métricas de Qualidade:** Como sabemos que uma resposta é boa? Quais são as regras para validar a saída?
  - *Exemplo:* "1. O resumo DEVE ter menos de 100 palavras. 2. DEVE mencionar o diagnóstico principal. 3. NÃO DEVE incluir informações pessoais de contato (LGPD). 4. A linguagem DEVE ser clara para um profissional de saúde."
- **Parâmetros Recomendados (Opcional):** Sugestões de parâmetros para a chamada da API do LLM.
  - *Exemplo:* "Temperatura: 0.3 (para respostas mais factuais)."

## 5. Notas Adicionais
- **Instruções:** Qualquer outra informação relevante para a implementação, como dependências, casos extremos a serem observados, ou lições aprendidas em testes anteriores.
- **Exemplo:** "Atenção: o prompt pode ter dificuldade com abreviações médicas muito antigas. Considerar um passo de pré-processamento no texto de entrada."
