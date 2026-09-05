# AI Tools Testing & Evaluation

Este repositório documenta a avaliação de diversas ferramentas, métodos e agentes de Inteligência Artificial voltados para o apoio ao desenvolvimento de software. A estrutura foi criada para ser expansível, permitindo a adição de novas ferramentas no futuro.

## Estrutura de Diretórios

- `docs/assistants/`: Ferramentas focadas em pair programming, edição de código e interfaces CLI.
- `docs/methods/`: Frameworks e metodologias para estruturar o trabalho com IAs.
- `docs/agents/`: Agentes autônomos e orquestradores que operam com maior independência.
- `docs/analytics/`: Ferramentas de observabilidade, telemetria e análise de uso de IA.

## Avaliação de Ferramentas por Categoria

### 1. Assistentes de Código (IDE & CLI)
Focados em pair programming, geração de código e interação rápida via editor ou terminal.

| Ferramenta | Descrição Principal | IDE | CLI | OpenAI | Anthropic | Google AI | OpenRouter | Plano Free |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [Claude Code](./docs/assistants/claude-code.md) | Plataforma agentic oficial da Anthropic (CLI + IDE + Agent View). | ✅ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ (API) |
| [Cursor](./docs/assistants/cursor.md) | IDE AI-first com Background Agents e BugBot. | ✅ | ❌ | ✅ | ✅ | ✅ | ⚠️ (via API custom) | ✅ (Hobby) |
| [OpenAI Codex](./docs/assistants/codex-cli.md) | Plataforma agentic da OpenAI (CLI + Desktop App). | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ (API) |
| [Open Codex](./docs/assistants/open-codex.md) | Fork comunitário do Codex CLI, multi-modelo. | ❌ | ✅ | ✅ | ✅ (via OR) | ✅ | ✅ | ✅ (Ollama) |
| [Google Antigravity](./docs/assistants/google-antigravity.md)| Plataforma agent-first do DeepMind (IDE + CLI + SDK). | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | ✅ (Preview) |

### 2. Agentes Autônomos e Orquestradores
Sistemas com maior autonomia, capazes de gerenciar múltiplas tarefas e manter estado persistente.

| Agente | Descrição Principal | OpenAI | Anthropic | Google AI | OpenRouter | Free / Open Source |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| [Paperclip](./docs/agents/paperclip.md) | Orquestrador BYOA com org-chart e heartbeats. | ✅ | ✅ | ✅ | ✅ | ✅ (OSS) |
| [Hermes](./docs/agents/hermes.md) | Agente auto-evolutivo com Skills e Kanban. | ✅ | ✅ | ✅ | ✅ | ✅ (OSS) |
| [OpenHands](./docs/agents/openhands.md) | IA Engenheira de Software com Agent Control Plane. | ✅ | ✅ | ✅ | ✅ | ✅ (OSS + Cloud) |
| [Google Antigravity](./docs/assistants/google-antigravity.md) | Agente de codificação com Mission Control e subagentes. | ✅ | ✅ | ✅ | ❌ | ✅ (Preview) |

### 3. Métodos e Toolkits
Estruturas de trabalho, metodologias e APIs para organizar o uso de IAs.

| Método / Toolkit | Descrição Principal | Agnóstico de Modelo? | Foco / Caso de Uso |
| :--- | :--- | :---: | :--- |
| [BMAD](./docs/methods/bmad.md) | Metodologia Agile AI-Driven (v6.x com BMB). | ✅ Sim | Estruturação de papéis, documentação e redução de alucinações. |
| [Pi](./docs/methods/pi.md) | Toolkit CLI com TUI rica (Earendil Works). | ✅ Sim | Construção de agentes customizados com extensões e hooks. |
| [CrewAI](./docs/methods/crewai.md) | Framework Crews + Flows com AMP enterprise. | ✅ Sim | Automação multi-agente, Flows event-driven e governança. |
| [Traycer AI](./docs/methods/traycer.md) | Camada de orquestração spec-first para agentes. | ✅ Sim | Planejamento estruturado, handoff e verificação de código. |

### 4. Analytics e Observabilidade
Ferramentas focadas em monitorar, analisar e melhorar o uso de assistentes de IA e engenharia agentic.

| Ferramenta | Descrição Principal | Local/Privado | Extensão IDE | Foco / Caso de Uso |
| :--- | :--- | :---: | :---: | :--- |
| [AI Engineer Coach](./docs/analytics/ai-engineering-coach.md) | Extensão VS Code para análise de logs de assistentes de IA. | ✅ Sim | ✅ (VS Code) | Melhoria contínua, detecção de anti-padrões e métricas agentic. |

---

## Mudanças e Evoluções das Ferramentas (2025–2026)

A tabela abaixo resume as principais evoluções e novidades que cada ferramenta incorporou ao longo de 2025–2026:

| Ferramenta | Estado Inicial | Estado Atual (2026) | Principais Mudanças |
| :--- | :--- | :--- | :--- |
| **Claude Code** | CLI puro com Claude 3.7 Sonnet | Plataforma multi-superfície (CLI + IDE + Agent View) | Extensões VS Code/JetBrains, Goal Mode (`/goal`), Routines, Plugins, Agent SDK, Remote Control, janela de contexto de 1M tokens |
| **Cursor** | IDE com autocompletar e Composer | Plataforma de agentes assíncronos (v3.5+) | Background Agents na nuvem, BugBot (revisão em PRs), Automations multi-repo e no-repo, integração Jira, Composer 2.5 |
| **OpenAI Codex** | Tradutor de linguagem natural → bash | Plataforma agentic (CLI + Desktop App) com GPT-5.5 | Goal Mode de longa duração, Computer Use nativo, Codex Security, Appshots visuais, plugins (Sentry/Datadog), suporte a servidores MCP |
| **Open Codex** | Fork do Codex CLI | Fork comunitário leve, open-source e modular | Foco em privacidade e zero vendor lock-in, modo Full Auto iterativo, sandboxing via Docker/Seatbelt, suporte nativo a Ollama/vLLM |
| **Google Antigravity** | IDE agent-first (nov/2025) | Antigravity 2.0: App Standalone + IDE + CLI + SDK | Central de controle desktop desacoplada, subagentes dinâmicos paralelos, Planning Mode com artefatos, Scheduled Tasks (`/schedule`), JSON Hooks e browser agent |
| **Paperclip** | Orquestrador de agentes BYOA | Plataforma operacional multi-agente (paperclip.ing) | Org-Chart visual de agentes com hierarquias, Heartbeat System persistente, approval workflows, servidor MCP nativo e perfis de custo por modelo |
| **Hermes** | Agente CLI com Skills | Agente auto-evolutivo (Nous Research v0.15+) | Skills auto-evolutivas (DSPy/GEPA), 90+ skills bundled, Kanban multi-agente durável, Computer Use universal, 5+ canais de mensageria, exportação de trajetórias MLOps |
| **OpenHands** | Agente autônomo em Docker (OpenDevin) | Engenheiro de software corporativo (70k+ ⭐, All-Hands-AI) | Agent Control Plane empresarial, Planning Mode (`PLAN.md`), aceleração de sandbox KVM, orquestração em Kubernetes, OpenHands Cloud SaaS |
| **BMAD** | Metodologia de papéis + Markdown | Framework ágil v6.x (Core/Method/Builder) | Combate ao "vibe coding" via artefatos Markdown, workflows por personas especializadas, Scale-Adaptive Intelligence (Quick/Standard/Enterprise) e suporte cross-platform |
| **Pi** | Toolkit CLI `@mariozechner` | Toolkit TUI e CLI sob `@earendil-works` (v0.74+) | Migração de namespace para `@earendil-works`, TUI interativa avançada, roteamento via `models.json` (OpenRouter/Together AI), geração de imagens e session branching |
| **CrewAI** | Framework Python para Crews | Plataforma enterprise Crews + Flows + AMP | Dualidade Crews colaborativas e Flows event-driven, Agent Management Platform (AMP) com RBAC e tracing, integração MCP nativa e protocolo A2A |
| **Traycer AI** | - | Camada de orquestração e governança spec-first | Especificações formais pré-código contra vibe coding, handoff inteligente para Cursor/Claude Code/Windsurf, motor de verificação fechada e persistência de intenção |
| **AI Engineer Coach** | - | Extensão de observabilidade e coaching local (Microsoft) | Análise local e privada de logs no VS Code, detecção contínua de mais de 45 anti-padrões, telemetria agentic de código, Skill Discovery e auditoria de contexto |

---

*Para sugerir ou adicionar novas ferramentas, crie o documento correspondente na pasta adequada e atualize esta tabela.*
