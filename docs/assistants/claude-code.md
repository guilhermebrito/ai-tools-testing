# Claude Code

> [!NOTE]
> O Claude Code evoluiu de um assistente CLI puramente de terminal para uma **plataforma agentic multi-superfície completa**, com suporte nativo a IDEs (VS Code e JetBrains), Agent View centralizado, sistema de plugins e orquestração autônoma via Goal Mode. Com a introdução do **Claude 4.5 Sonnet** como modelo padrão, suporte multi-modelo via OpenRouter, integração oficial com GitHub Actions e o novo plano Claude Max, a ferramenta combina raciocínio estendido (*extended thinking*) de ponta com alta flexibilidade para fluxos profissionais e CI/CD.

## Visão Geral
O **Claude Code** é a ferramenta agentic oficial de desenvolvimento de software da **Anthropic**, projetada para atuar como um engenheiro parceiro diretamente no fluxo do desenvolvedor. Alimentada pelos modelos de ponta da família Claude — tendo o **Claude 4.5 Sonnet** (lançado em setembro de 2026) como modelo padrão, com capacidades aprofundadas de raciocínio estendido (*extended thinking*) e performance superior em código, além de Claude 3.7 Sonnet, Claude Sonnet 4 e Opus com Fast Mode —, a ferramenta suporta contextos de até **1 milhão de tokens** e conta com melhorias contínuas de latência reduzida e gerenciamento otimizado de contexto. Opera tanto no terminal (*terminal-first*) quanto integrada em editores, esteiras de CI/CD e painéis multi-agente.

## Principais Funcionalidades e Novidades (2025–2026)
- **Claude 4.5 Sonnet como Padrão (Setembro 2026):** Modelo padrão com capacidades de *extended thinking*, oferecendo desempenho de referência na geração, refatoração profunda e depuração de código complexo.
- **Suporte Multi-Modelo via OpenRouter:** Flexibilidade para rotear requisições para modelos de terceiros por meio da integração com o OpenRouter, permitindo o uso de modelos especializados ou alternativas open-weight.
- **Custom Slash Commands:** Criação de comandos de barra personalizados (`/comando`) para padronizar e automatizar rotinas customizadas do desenvolvedor ou da equipe.
- **Integração com GitHub Actions:** Ação oficial (`anthropics/claude-code-action`) para automação de CI/CD, permitindo executar revisões de código em PRs, resolver issues de forma autônoma e rodar tarefas diretamente na pipeline.
- **Melhorias de Performance e Contexto:** Otimizações que proporcionam menor latência nas respostas e gerenciamento aprimorado de contexto em sessões longas e complexas.
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
- **Raciocínio Lógico e Refatoração:** Aproveita a profundidade analítica e o raciocínio estendido dos modelos Claude mais recentes (notadamente o Claude 4.5 Sonnet) para resolução de problemas arquiteturais complexos.
- **Janela de Contexto Gigante (1M Tokens):** Capacidade de analisar repositórios inteiros sem perda de contexto ou fragmentação, agora com melhor gerenciamento dinâmico.
- **Flexibilidade Operacional:** Cobertura do fluxo completo — do terminal minimalista a extensões de IDE, pipelines de CI/CD e orquestração de subagentes.

### Limitações
- **Ecossistema e Suporte a Terceiros:** Agora parcialmente agnóstico a modelos graças ao suporte multi-modelo via OpenRouter, embora as otimizações nativas de ferramentas e prompts continuem projetadas primariamente para os modelos Claude da Anthropic.
- **Consumo de Tokens:** Sessões longas em repositórios massivos com Goal Mode e raciocínio estendido podem gerar consumo elevado de tokens e custos de API.

## Casos de Uso
- Auditoria, modernização e refatoração de bases legadas com visão de contexto integral.
- Execução autônoma de migrações e correções de bugs complexos via Goal Mode.
- Automação de pipelines de CI/CD, triage de issues e revisão de Pull Requests via Claude Code GitHub Actions.
- Padronização de comandos e automações repetitivas via Custom Slash Commands.
- Automação de pipelines de desenvolvimento com Routines (preparação de PRs e relatórios técnicos).
- Construção de fluxos customizados de agentes de software via Claude Agent SDK.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário (desenvolvido pela Anthropic).
- **Preço:**
  - Instalação gratuita via pacote CLI (`@anthropic-ai/claude-code`).
  - Requer assinatura paga Anthropic ou faturamento por uso:
    - **Claude Pro:** Acesso individual aos modelos avançados.
    - **Claude Max Plan:** Novo plano com limites de uso significativamente superiores (*high-limit tiers*), projetado para desenvolvedores profissionais e fluxos intensivos.
    - **Claude Team & Enterprise:** Planos para equipes e corporações com controles administrativos e faturamento centralizado.
    - **Anthropic API Console:** Pagamento sob demanda pelo consumo de tokens.
- **Agnóstico de Provedor:** Parcialmente agnóstico (suporta modelos de terceiros via integração com OpenRouter, além dos modelos nativos da Anthropic).

## Links Úteis
- **Documentação Oficial:** [https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- **Pacote NPM:** [https://www.npmjs.com/package/@anthropic-ai/claude-code](https://www.npmjs.com/package/@anthropic-ai/claude-code)
- **Claude Code GitHub Action:** [https://github.com/anthropics/claude-code-action](https://github.com/anthropics/claude-code-action)
