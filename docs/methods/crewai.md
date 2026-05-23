# CrewAI

> [!NOTE]
> O CrewAI evoluiu de um framework de agentes colaborativos para uma **plataforma enterprise de orquestração agentic**, combinando Crews autônomas com Flows estruturados e um Agent Management Platform (AMP) de produção.

## Visão Geral
O **CrewAI** é um framework poderoso em Python para estruturar, orquestrar e gerenciar "times" (crews) de agentes de IA autônomos. Em 2026, a plataforma expandiu-se para atender demandas enterprise com o lançamento do **CrewAI AMP (Agent Management Platform)**, criando uma distinção clara entre o core open-source e a infraestrutura de produção.

---

## Funcionalidades Principais

### Crews — Colaboração Autônoma
*   **Design Baseado em Papéis (Role-based):** Definição de agentes com papéis específicos (ex: 'Engenheiro Sênior', 'Especialista de QA', 'Product Manager'), cada um com *backstory* e meta focada.
*   **Delegação e Colaboração:** Agentes delegam subtarefas entre si, discutem e compartilham contexto em tempo real, viabilizando resolução de problemas em múltiplas etapas.
*   **Agnosticismo de Modelos:** Flexibilidade total de LLMs — um time pode ter o 'Desenvolvedor' usando Claude Sonnet, o 'Revisor' usando GPT-4o e o 'Pesquisador' usando um Llama local.

### Flows — Orquestração de Precisão
*   **Arquitetura Event-Driven:** Definição de caminhos de execução precisos com lógica condicional, loops e branching.
*   **Gestão de Estado e Persistência:** Flows gerenciam estado nativamente entre etapas, permitindo workflows resumíveis e consistência de dados para tarefas enterprise de longa duração.
*   **Integração Crews + Flows:** Flows atuam como "gerente" do processo geral, enquanto Crews são embutidas para lidar com tarefas colaborativas e autônomas específicas.

### CrewAI AMP — Plataforma Enterprise
*   **Control Plane Centralizado:** Interface unificada para gerenciar, monitorar e escalar agentes entre departamentos e unidades de negócio.
*   **Tracing & Observabilidade:** Visibilidade em tempo real de ações dos agentes, interpretação de tarefas, chamadas de ferramentas e outputs finais.
*   **Governança & Segurança:** Suporte a RBAC (Role-Based Access Control), audit logs e opções de deploy seguro (cloud, on-premise ou local).
*   **Resiliência:** Checkpointing, lineage tracking e recuperação automática de falhas para workflows enterprise robustos.

### Ecossistema e Integrações
*   **Model Context Protocol (MCP):** Integração nativa com MCP para comunicação com ferramentas e fontes de dados externas sem código de integração custom.
*   **Suporte Multimodal Nativo:** File handling aprimorado e structured outputs cross-provider.
*   **Agent-to-Agent (A2A):** Comunicação avançada entre agentes com metadata enrichment e mecanismos de transporte sofisticados.
*   **Integração LangChain:** Ecossistema nativo de ferramentas (busca web, execução de código, bancos de dados, APIs).

---

## Pontos Fortes
*   **Dualidade Crews + Flows:** Combina a criatividade da colaboração autônoma (Crews) com a previsibilidade de workflows estruturados (Flows).
*   **Production-Grade:** A suite AMP fornece a infraestrutura necessária para levar agentes de protótipos a produção real.
*   **Comunidade Massiva:** Um dos frameworks de agentes mais adotados globalmente.

---

## Casos de Uso
*   Geração de código estruturado: um agente escreve, outro revisa, um terceiro cria testes.
*   Automação de processos complexos com múltiplas etapas de revisão e decisão.
*   Pipelines de dados (pesquisa web, sumarização, formatação) com Flows event-driven.
*   Operações enterprise em finanças, RH e supply chain com governança e compliance.

---

## Status
*   **Open Source:** Sim (Licença MIT).
*   **Agnóstico de Modelo:** Sim.

---

## Links Úteis
*   **Site Oficial / Documentação:** [https://www.crewai.com/](https://www.crewai.com/)
*   **Repositório Oficial (GitHub):** [https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)
