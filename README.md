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
| [Claude Code](./docs/assistants/claude-code.md) | Plataforma agentic oficial da Anthropic (CLI + IDE + Agent View). | ✅ | ✅ | ❌ | ✅ | ❌ | ⚠️ (via OpenRouter) | ❌ (API / Max) |
| [Cursor](./docs/assistants/cursor.md) | IDE AI-first com Background Agents e BugBot (v4.0). | ✅ | ❌ | ✅ | ✅ | ✅ | ⚠️ (via API custom) | ✅ (Hobby) |
| [OpenAI Codex](./docs/assistants/codex-cli.md) | Plataforma agentic da OpenAI (CLI + Desktop App + ChatGPT). | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ (API / Plus) |
| [Open Codex](./docs/assistants/open-codex.md) | Fork comunitário do Codex CLI, multi-modelo. | ❌ | ✅ | ✅ | ✅ (via OR) | ✅ | ✅ | ✅ (Ollama) |
| [Google Antigravity](./docs/assistants/google-antigravity.md)| Plataforma agent-first do DeepMind (IDE + CLI + SDK). | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | ✅ (Preview) |

### 2. Agentes Autônomos e Orquestradores
Sistemas com maior autonomia, capazes de gerenciar múltiplas tarefas e manter estado persistente.

| Agente | Descrição Principal | OpenAI | Anthropic | Google AI | OpenRouter | Free / Open Source |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| [Paperclip](./docs/agents/paperclip.md) | Orquestrador BYOA com org-chart e heartbeats. | ✅ | ✅ | ✅ | ✅ | ✅ (OSS) |
| [Hermes](./docs/agents/hermes.md) | Agente auto-evolutivo com Skills (100+) e Kanban. | ✅ | ✅ | ✅ | ✅ | ✅ (OSS + Pro) |
| [OpenHands](./docs/agents/openhands.md) | IA Engenheira de Software (SWE-bench líder, Cloud SaaS). | ✅ | ✅ | ✅ | ✅ | ✅ (OSS + Cloud) |
| [Google Antigravity](./docs/assistants/google-antigravity.md) | Agente de codificação com Mission Control e subagentes. | ✅ | ✅ | ✅ | ❌ | ✅ (Preview) |

### 3. Métodos e Toolkits
Estruturas de trabalho, metodologias e APIs para organizar o uso de IAs.

| Método / Toolkit | Descrição Principal | Agnóstico de Modelo? | Foco / Caso de Uso |
| :--- | :--- | :---: | :--- |
| [BMAD](./docs/methods/bmad.md) | Metodologia Agile AI-Driven (v6.x – v7.0). | ✅ Sim | Estruturação de papéis, personas especializadas e integração MCP. |
| [Pi](./docs/methods/pi.md) | Toolkit CLI com TUI rica (Earendil Works v0.80+ / v1.0). | ✅ Sim | Construção de agentes customizados, split-screen e inferência rápida (Groq/Cerebras). |
| [CrewAI](./docs/methods/crewai.md) | Framework Crews + Flows 2.0 (Marco v1.0). | ✅ Sim | Automação multi-agente assíncrona, observabilidade nativa e Marketplace de Crews. |
| [Traycer AI](./docs/methods/traycer.md) | Camada de orquestração spec-first (Traycer 2.0). | ✅ Sim | Visual Spec Editor, verificação de código, integração GitHub e multi-agente. |

### 4. Analytics e Observabilidade
Ferramentas focadas em monitorar, analisar e melhorar o uso de assistentes de IA e engenharia agentic.

| Ferramenta | Descrição Principal | Local/Privado | Extensão IDE | Foco / Caso de Uso |
| :--- | :--- | :---: | :---: | :--- |
| [AI Engineer Coach](./docs/analytics/ai-engineering-coach.md) | Extensão VS Code para análise de logs de assistentes de IA. | ✅ Sim | ✅ (VS Code) | Melhoria contínua, detecção de 55+ anti-padrões, suporte multi-assistente e Team Mode. |

---

## Mudanças e Evoluções das Ferramentas (2025–2026)

A tabela abaixo resume as principais evoluções e novidades que cada ferramenta incorporou ao longo de 2025–2026:

| Ferramenta | Estado Inicial | Estado Atual (Outubro 2026) | Principais Mudanças |
| :--- | :--- | :--- | :--- |
| **Claude Code** | CLI puro com Claude 3.7 Sonnet | Plataforma multi-superfície (CLI + IDE + Agent View) | Claude 4.5 Sonnet como padrão, suporte multi-modelo via OpenRouter, GitHub Actions oficial, Custom Slash Commands, plano Claude Max |
| **Cursor** | IDE com autocompletar e Composer | Plataforma de agentes assíncronos (v4.0) | Max Mode com raciocínio profundo, Memories persistentes, Background Agents tolerantes a falhas, integrações Linear/Notion, BugBot com segurança/performance, plano Ultra |
| **OpenAI Codex** | Tradutor de linguagem natural → bash | Plataforma agentic unificada (o3-pro e Codex-mini) | Modelos o3-pro e Codex-mini, workflows multi-agente paralelos, sandboxing granular avançado, integração profunda no ChatGPT e convergência com Copilot |
| **Open Codex** | Fork do Codex CLI | Fork comunitário leve, open-source e modular | Suporte aos modelos open-weights Llama 3.3 e DeepSeek V3, manutenção focada em privacidade, zero telemetria e estabilidade |
| **Google Antigravity** | IDE agent-first (nov/2025) | Antigravity 2.0: App Standalone + IDE + CLI + SDK | Modelos Gemini 2.5 Pro e Flash, lançamento do Gemini CLI open-source (Apache 2.0), aba Automations renovada, integração fluida com Google AI Studio e Vertex AI |
| **Paperclip** | Orquestrador de agentes BYOA | Plataforma operacional multi-agente (paperclip.ing) | Templates de Org-Chart prontos, melhorias no servidor MCP para cross-agent communication, dashboard com métricas de custos granulares, novos adaptadores modulares |
| **Hermes** | Agente CLI com Skills | Agente auto-evolutivo (Nous Research v0.16+) | 100+ skills (novas categorias DevOps/Cloud e Observabilidade), loop 60% mais rápido, Kanban com auto-priorização e anti-zombie, suporte Claude 4.5 e anúncio do Hermes Pro |
| **OpenHands** | Agente autônomo em Docker (OpenDevin) | Engenheiro de software de ponta (70k+ ⭐, SWE-bench líder) | Destaque no benchmark SWE-bench, GitHub Resolver para issues e PRs automáticos, ciclo v0.40+, OpenHands Cloud SaaS e suporte a Claude 4.5 / GPT-5.5 |
| **BMAD** | Metodologia de papéis + Markdown | Framework ágil v6.x preparando v7.0 | Anúncio do BMAD v7.0 para integração agentic nativa, novas personas especializadas (Security Engineer e Data Engineer), exploração de integração com servidores MCP |
| **Pi** | Toolkit CLI `@mariozechner` | Toolkit TUI e CLI sob `@earendil-works` (v0.80+) | TUI com split-screen para múltiplas conversas, suporte aos endpoints rápidos da Groq e Cerebras, novos hooks de ciclo de vida (`on_session_start`/`end`), preview do Pi Studio |
| **CrewAI** | Framework Python para Crews | Framework de produção Crews + Flows 2.0 (v1.0) | Marco oficial CrewAI v1.0, Flows 2.0 assíncrono com estados avançados, CrewAI CLI robusto, observabilidade nativa, Marketplace de Crews e 80k+ ⭐ |
| **Traycer AI** | - | Camada de orquestração spec-first (Traycer 2.0) | Visual Spec Editor interativo, integração nativa GitHub (PRs e Issues), orquestração multi-agente ampliada (Cursor, Claude Code, Windsurf), Verification Dashboard e plano free expandido |
| **AI Engineer Coach** | - | Extensão de observabilidade e coaching local (Microsoft) | Detecção expandida para 55+ anti-padrões, suporte a logs de Claude Code, Cursor e Antigravity, painel de tendências analíticas e Team Mode experimental |

---

*Para sugerir ou adicionar novas ferramentas, crie o documento correspondente na pasta adequada e atualize esta tabela.*
