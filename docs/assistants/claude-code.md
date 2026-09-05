# Claude Code

> [!NOTE]
> O Claude Code evoluiu de um assistente CLI puramente de terminal para uma **plataforma agentic multi-superfície completa**, com suporte nativo a IDEs (VS Code e JetBrains), Agent View centralizado, sistema de plugins e orquestração autônoma via Goal Mode.

## Visão Geral
O **Claude Code** é a ferramenta agentic oficial de desenvolvimento de software da **Anthropic**, projetada para atuar como um engenheiro parceiro diretamente no fluxo do desenvolvedor. Alimentada pelos modelos de ponta da família Claude (incluindo Claude 3.7 Sonnet, Claude Sonnet 4 e Opus com Fast Mode), a ferramenta suporta contextos de até **1 milhão de tokens** e opera tanto no terminal (*terminal-first*) quanto integrada em editores e painéis de múltiplos agentes.

## Principais Funcionalidades e Novidades (2025–2026)
- **Interfaces Multi-Superfície:**
  - **CLI Nativo:** Opera diretamente no shell para exploração de repositórios, edição concorrente de arquivos, execução de testes e commits.
  - **Extensões IDE (VS Code & JetBrains):** Extensões nativas com visualização de diffs interativa, compartilhamento de contexto (arquivos abertos, diagnósticos de linter, erros de compilação) e atalhos rápidos (`Cmd+Esc`).
  - **Agent View:** Painel centralizado para gerenciar múltiplas sessões concorrentes de agentes, facilitando a supervisão de tarefas paralelas.
- **Autonomia Avançada com Goal Mode (`/goal`):** Permite definir metas de alto nível (ex: "fazer toda a suíte de testes de autenticação passar"), permitindo que o agente trabalhe de forma autônoma e iterativa até cumprir o critério estabelecido.
- **Auto Mode e Classificador de Permissões:** Sistema de segurança baseado em IA que avalia e auto-aprova chamadas de ferramentas seguras, minimizando interrupções manuais sem comprometer a segurança.
- **Routines & Automações:** Automações reutilizáveis configuradas para disparos agendados, webhooks ou eventos de CI/CD (ex: geração noturna de PRs ou auditoria de dependências).
- **Remote Control:** Capacidade de iniciar sessões no ambiente local e monitorar/retomar a execução remotamente através de interfaces web ou mobile.
- **Extensibilidade e Plugins:**
  - **Plugins:** Carregamento de pacotes externos via `--plugin-dir` ou `--plugin-url` (suporte a `.zip`), integrando ferramentas de terceiros e especializações.
  - **Hooks de Ciclo de Vida:** Execução de scripts automáticos pré e pós ações (ex: rodar linters antes de commits ou testes após alterações).
  - **Claude Agent SDK:** SDK completo para criar subagentes especializados e fluxos multi-agente usando a mesma memória e arquitetura de ferramentas do Claude Code.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Raciocínio Lógico e Refatoração:** Aproveita a profundidade analítica dos modelos Claude mais recentes para resolução de problemas arquiteturais complexos.
- **Janela de Contexto Gigante (1M Tokens):** Capacidade de analisar repositórios inteiros sem perda de contexto ou fragmentação.
- **Flexibilidade Operacional:** Cobertura do fluxo completo — do terminal minimalista a extensões de IDE e orquestração de subagentes.

### Limitações
- **Restrito ao Ecossistema Anthropic:** Sem suporte nativo direto a modelos de outros provedores (OpenAI, Google, open-weights).
- **Consumo de Tokens:** Sessões longas em repositórios massivos com Goal Mode podem gerar consumo elevado de API.

## Casos de Uso
- Auditoria, modernização e refatoração de bases legadas com visão de contexto integral.
- Execução autônoma de migrações e correções de bugs complexos via Goal Mode.
- Automação de pipelines de desenvolvimento com Routines (preparação de PRs e relatórios técnicos).
- Construção de fluxos customizados de agentes de software via Claude Agent SDK.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário (desenvolvido pela Anthropic).
- **Preço:** Instalação gratuita (via `@anthropic-ai/claude-code`); requer assinatura paga Anthropic (Pro, Max, Team ou Enterprise) ou pagamento por uso via API Console Anthropic.
- **Agnóstico de Provedor:** Não (exclusivo para modelos Claude).

## Links Úteis
- **Documentação Oficial:** [https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- **Pacote NPM:** [https://www.npmjs.com/package/@anthropic-ai/claude-code](https://www.npmjs.com/package/@anthropic-ai/claude-code)
