# Paperclip

> [!NOTE]
> O Paperclip não é um agente — é o **controle de missão** que gerencia, monitora e orquestra times inteiros de agentes autônomos como uma empresa orientada por IA.

## Visão Geral
O **Paperclip** (paperclip.ing) é uma plataforma open-source de orquestração UI-driven para agentes de Inteligência Artificial, lançada em março de 2026. Diferente de frameworks que constroem agentes, o Paperclip adota a filosofia **"Bring Your Own Agent" (BYOA)** — ele integra agentes já existentes (Claude Code, Codex, Hermes, scripts Bash ou Python) e os organiza em uma estrutura empresarial funcional com cargos, relatórios hierárquicos e filas de trabalho.

---

## Como Funciona

### Estrutura Organizacional
*   **Org Chart de Agentes:** Interface onde se definem papéis (CEO, Engineering, Marketing, QA, Suporte), linhas de reporte e job descriptions para cada agente de IA, simulando a estrutura de uma empresa real.
*   **Heartbeat System:** Sistema de sinais vitais agendados onde os agentes "acordam" em intervalos regulares, consultam suas filas de trabalho, executam tarefas e reportam progresso — prevenindo consumo desnecessário de tokens e mantendo continuidade entre sessões.

### Governança e Controle
*   **Gestão de Orçamento:** Limites de gastos por agente com auto-pausa automática ao atingir o limite, evitando consumo excessivo de API.
*   **Audit Logs:** Logs de auditoria para rastreabilidade de decisões tomadas pelos agentes.
*   **Approval Workflows:** Fluxos de aprovação para ações estratégicas, garantindo que agentes não atuem sem supervisão em decisões críticas.

### Infraestrutura
*   **Dashboard Unificado (React):** Painel "CEO Dashboard" para rastrear progresso, monitorar gastos de tokens e gerenciar a frota inteira de agentes em uma única interface.
*   **Arquitetura Extensível:** Sistema baseado em plugins e servidor **MCP (Model Context Protocol)**, permitindo comunicação com diversos runtimes e ferramentas de agentes sem código de integração bespoke.
*   **Self-Hosting:** Suporte completo a self-hosting via Docker (ex: VPS/VDS em provedores como Contabo), garantindo controle total sobre dados e governança.

---

## Evoluções Recentes (2026)
*   **Otimização de Modelos:** Introdução de "cheaper model profiles" para recovery e execução de tarefas, usando o modelo correto para cada etapa para otimizar custos.
*   **Adaptadores Expandidos:** Expansão dos adaptadores core (incluindo suporte ao Hermes) e refinamento do servidor MCP.
*   **Comunidade:** Crescimento rápido com dezenas de milhares de GitHub stars desde o lançamento em março de 2026.

---

## Pontos Fortes
*   **Resolução do Problema "Stateless":** Garante que agentes mantenham memória e contexto entre sessões. Se a máquina reiniciar, o agente volta de onde parou.
*   **Orquestração Visual:** Dashboard completo para ver quem (qual agente) está fazendo o que, e aprovar o trabalho antes de merge.
*   **Agnosticismo Total:** Funciona com qualquer agente, qualquer provedor de modelo, qualquer infraestrutura.

---

## Casos de Uso
*   Operar uma "empresa de IA" com múltiplos agentes assumindo papéis distintos (marketing, pesquisa, QA, desenvolvimento) em paralelo.
*   Automação de tarefas longas de infraestrutura que demoram dias para concluir.
*   Governança e controle de custos em operações multi-agente.

---

## Links Úteis
*   **Site Oficial:** [https://paperclip.ing/](https://paperclip.ing/)
*   **Repositório Oficial (GitHub):** [https://github.com/paperclip-dev/paperclip](https://github.com/paperclip-dev/paperclip)
