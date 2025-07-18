# Exemplo de Preenchimento: Canvas de Planejamento de Escalabilidade

_(Este canvas é preenchido como resultado da "Ação Imediata" identificada no canvas de métricas acima)_

- **1. Objetivo da Escalabilidade**

    - Preparar a infraestrutura do assistente para suportar o lançamento para todas as 10 recepcionistas da clínica, mantendo o tempo de resposta médio abaixo de 2 segundos.

- **2. Volume Esperado de Interações**

    - **Cenário Atual:** 50 interações/dia (2 usuários).
    - **Cenário Escalado:** ~500 interações/dia (10 usuários), com picos de 100 interações/hora.

- **3. Requisitos de Infraestrutura**

    - **Servidores:** Adicionar 2 instâncias do contêiner do "Serviço de IA" e configurar um load balancer.
    - **API do LLM:** Aumentar o limite de requisições por minuto (RPM) no plano da API do Google.

- **4. Estratégias de Escalabilidade**

    - **Horizontal:** Adicionar mais instâncias do serviço de IA para distribuir a carga.
    - **Cache:** Implementar cache em memória (Redis) para as perguntas mais frequentes, reduzindo chamadas à API do LLM.

- **5. Custo Estimado**

    - **Servidores:** + R$ 800/mês.
    - **API do LLM:** + R$ 1.200/mês (estimado com base no novo volume).
    - **Cache (Redis):** + R$ 200/mês.

- **6. Riscos e Mitigação**

    - **Risco:** Atingir o limite da API do LLM em horários de pico.
    - **Mitigação:** Implementar "rate limiting" e um sistema de retentativas (retries) com "exponential backoff" no nosso backend.

- **7. Monitoramento de Escalabilidade**

    - Configurar alertas no Datadog para uso de CPU > 80% nas instâncias do serviço de IA e para latência da API > 2s.

- **8. Plano de Teste em Ambiente Escalado**

    - Realizar testes de carga com a ferramenta k6, simulando 100 usuários/hora, para validar a distribuição do tráfego pelo load balancer e o desempenho do cache.
