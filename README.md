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

A tabela abaixo resume as principais evoluções que cada ferramenta passou desde seu lançamento até maio de 2026:

| Ferramenta | Estado Inicial | Estado Atual (Maio 2026) | Principais Mudanças |
| :--- | :--- | :--- | :--- |
| **Claude Code** | CLI puro com Claude 3.7 Sonnet | Plataforma multi-superfície (CLI + IDE + Agent View) | Extensões VS Code/JetBrains, Goal Mode, Routines, Plugins, Agent SDK, Remote Control, 1M tokens |
| **Cursor** | IDE com autocompletar e Composer | Plataforma de agentes assíncronos (v3.5) | Background Agents na nuvem, BugBot, Automations multi-repo, Jira integration, Composer 2.5 |
| **OpenAI Codex** | Tradutor de linguagem natural → bash | Plataforma agentic (CLI + Desktop App) com GPT-5.5 | Goal Mode, Computer Use, Codex Security, Plugins (Sentry/Datadog), MCP, Appshots |
| **Open Codex** | Fork do Codex CLI | Fork comunitário leve e estável | Mantém foco em agnósticismo de provedor e execução local segura (Ollama) |
| **Google Antigravity** | IDE agent-first (nov/2025) | Antigravity 2.0: App Standalone + CLI + SDK | App desktop independente, Agent Manager (Mission Control), subagentes dinâmicos, Scheduled Tasks, JSON Hooks |
| **Paperclip** | Orquestrador de agentes BYOA | Plataforma empresa de IA (lançada mar/2026) | Org-chart, heartbeats, approval workflows, MCP server, cheaper model profiles |
| **Hermes** | Agente CLI com Skills | Agente auto-evolutivo com Kanban multi-agente | Skills auto-evolutivas (DSPy/GEPA), Computer Use, 20+ plataformas de mensageria, agent loop 47% mais rápido |
| **OpenHands** | Agente autônomo em Docker (OpenDevin) | Plataforma enterprise (70k+ ⭐, $23.8M funding) | Agent Control Plane, Planning Mode, KVM sandbox, Kubernetes, OpenHands Cloud SaaS |
| **BMAD** | Metodologia de papéis + Markdown | Framework v6.x com 3 camadas (Core/Method/Builder) | Scale-adaptive intelligence, cross-platform (Cursor/Claude/Antigravity), BMad Builder |
| **Pi** | Toolkit CLI `@mariozechner` | Pi v0.74+ sob `@earendil-works` | Migração de namespace, OpenRouter routing, image generation, Together AI, hooks avançados |
| **CrewAI** | Framework Python para Crews | Plataforma enterprise com Crews + Flows + AMP | Flows event-driven, AMP (Control Plane, RBAC, tracing), MCP, A2A communication |
| **AI Engineer Coach** | - | Lançamento open-source | Ferramenta de observabilidade local para VS Code com detecção de 45+ anti-padrões e métricas agentic. |
| **Traycer AI** | - | Lançamento recente | Plataforma spec-first que atua como orquestrador e verificador entre o desenvolvedor e agentes de IA. |

---

*Para sugerir ou adicionar novas ferramentas, crie o documento correspondente na pasta adequada e atualize esta tabela.*
