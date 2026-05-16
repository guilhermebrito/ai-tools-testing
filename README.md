# AI Tools Testing & Evaluation

Este repositório documenta a avaliação de diversas ferramentas, métodos e agentes de Inteligência Artificial voltados para o apoio ao desenvolvimento de software. A estrutura foi criada para ser expansível, permitindo a adição de novas ferramentas no futuro.

## Estrutura de Diretórios

- `docs/assistants/`: Ferramentas focadas em pair programming, edição de código e interfaces CLI.
- `docs/methods/`: Frameworks e metodologias para estruturar o trabalho com IAs.
- `docs/agents/`: Agentes autônomos e orquestradores que operam com maior independência.

## Avaliação de Ferramentas por Categoria

### 1. Assistentes de Código (IDE & CLI)
Focados em pair programming, geração de código e interação rápida via editor ou terminal.

| Ferramenta | Descrição Principal | OpenAI | Anthropic | Google AI | OpenRouter | Plano Free |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| [Claude Code](./docs/assistants/claude-code.md) | Assistente oficial da Anthropic para o terminal. | ❌ | ✅ | ❌ | ❌ | ❌ (API) |
| [Cursor](./docs/assistants/cursor.md) | IDE AI-first baseada no VS Code. | ✅ | ✅ | ✅ | ⚠️ (via API custom) | ✅ (Básico) |
| [Codex CLI](./docs/assistants/codex-cli.md) | Tradutor de linguagem natural para bash. | ✅ | ❌ | ❌ | ❌ | ❌ (API) |
| [Open Codex](./docs/assistants/open-codex.md) | Fork CLI do Codex com suporte multi-modelo. | ✅ | ✅ (via OR) | ✅ | ✅ | ✅ (Ollama) |
| [Google Antigravity](./docs/assistants/google-antigravity.md)| Agente de codificação autônomo do DeepMind. | ❌ | ❌ | ✅ | ❌ | ❌ |

### 2. Agentes Autônomos e Orquestradores
Sistemas com maior autonomia, capazes de gerenciar múltiplas tarefas e manter estado persistente.

| Agente | Descrição Principal | OpenAI | Anthropic | Google AI | OpenRouter | Free / Open Source |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| [Paperclip](./docs/agents/paperclip.md) | Plataforma UI para orquestrar "times" de agentes. | ✅ | ✅ | ✅ | ✅ | ✅ (OSS) |
| [Hermes](./docs/agents/hermes.md) | Agente persistente focado em devs ("Skills"). | ✅ | ✅ | ✅ | ✅ | ✅ (OSS) |

### 3. Métodos e Toolkits
Estruturas de trabalho, metodologias e APIs para organizar o uso de IAs.

| Método / Toolkit | Descrição Principal | Agnóstico de Modelo? | Foco / Caso de Uso |
| :--- | :--- | :---: | :--- |
| [BMAD](./docs/methods/bmad.md) | Metodologia Agile AI-Driven. | ✅ Sim | Estruturação de papéis e redução de alucinações. |
| [Pi](./docs/methods/pi.md) | Toolkit CLI e API para criação de agentes. | ✅ Sim | Construção de agentes customizados. |

---

*Para sugerir ou adicionar novas ferramentas, crie o documento correspondente na pasta adequada e atualize esta tabela.*
