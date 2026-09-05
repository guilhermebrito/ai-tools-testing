# CrewAI

> [!NOTE]
> O CrewAI expandiu de um framework de times autônomos para uma **plataforma enterprise completa de orquestração agentic**, unindo a colaboração dinâmica das Crews, a previsibilidade determinística dos Flows e o plano de governança CrewAI AMP.

## Visão Geral
O **CrewAI** é um dos frameworks mais populares em Python para modelagem, orquestração e execução de sistemas multi-agente de Inteligência Artificial. A plataforma evoluiu para suportar fluxos de trabalho híbridos de produção, combinando a flexibilidade colaborativa de agentes com a robustez e determinismo de pipelines baseados em eventos (*Flows*), além de uma camada corporativa para controle e observabilidade (*AMP*).

## Principais Funcionalidades e Novidades (2025–2026)
- **Dualidade Crews + Flows:**
  - **Crews (Colaboração Autônoma):** Times de agentes com papéis (*roles*), metas (*goals*) e históricos (*backstories*) bem definidos que colaboram, delegam subtarefas e revisam o trabalho mútuo de maneira autônoma.
  - **Flows (Orquestração Event-Driven):** Controle de fluxo determinístico com ramificações, condicionais e loops explícitos. Permite gerenciar estados persistentes entre etapas e retomar execuções longas sem perder progresso.
- **CrewAI AMP (Agent Management Platform):**
  - Plataforma de controle de nível empresarial para governança centralizada, gerenciamento de permissões (*RBAC*), logs de auditoria e monitoramento de desempenho em múltiplos departamentos.
  - **Tracing & Observabilidade:** Rastreamento ponta a ponta de chamadas de ferramentas, latência, custos de inferência e árvores de decisão dos agentes.
  - **Resiliência e Checkpointing:** Gravação de estados intermediários e recuperação automática de falhas em processos críticos.
- **Integração Nativa com MCP (Model Context Protocol):**
  - Conexão simplificada com ferramentas externas, servidores locais de banco de dados e APIs via protocolo padronizado MCP, sem necessidade de adapters manuais.
- **Comunicação Agent-to-Agent (A2A):**
  - Protocolo padronizado para troca de mensagens e metadados estruturados entre agentes locais ou distribuídos em diferentes instâncias.
- **Alocação Heterogênea de Modelos:**
  - Atribuição independente de LLMs por papel: agentes analistas e arquitetos utilizam modelos topo de linha (Claude 3.7 Sonnet, GPT-4o), enquanto tarefas rotineiras de formatação ou parsing rodam em modelos rápidos e locais (Llama, Mistral).

## Pontos Fortes e Limitações
### Pontos Fortes
- **Equilíbrio entre Autonomia e Controle:** A combinação de Crews com Flows resolve o desafio de previsibilidade em pipelines de produção.
- **Ecossistema e Adoção Enterprise:** A suite AMP fornece recursos fundamentais para conformidade corporativa e segurança da informação.
- **Totalmente Agnóstico de Modelos:** Compatível com praticamente qualquer API ou servidor local (vLLM, Ollama) via LangChain e LiteLLM.

### Limitações
- **Curva de Latência:** Workflows multi-agente complexos com múltiplas rodadas de debate e revisão mútua podem requerer tempo de resposta considerável.
- **Complexidade Operacional:** Deploy enterprise com o AMP exige infraestrutura adicional de observabilidade e banco de dados.

## Casos de Uso
- Pipelines de desenvolvimento de software onde agentes desenvolvem, testam e realizam code review em cadeia.
- Automação de processos empresariais complexos (análise financeira, conformidade jurídica e pesquisa de mercado).
- Extração, enriquecimento e estruturação de dados em larga escala com pipelines event-driven.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT) para o framework core; oferta comercial para o CrewAI Enterprise/AMP.
- **Preço:** Framework gratuito; custos atrelados a consumo de tokens de LLM e licenciamento comercial da plataforma AMP.
- **Agnóstico de Provedor:** Sim (100% agnóstico).

## Links Úteis
- **Site Oficial / Documentação:** [https://www.crewai.com/](https://www.crewai.com/)
- **Repositório Oficial (GitHub):** [https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)
