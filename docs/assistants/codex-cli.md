# OpenAI Codex (Codex CLI & Desktop)

> [!NOTE]
> O Codex evoluiu de um tradutor pontual de comandos para uma **plataforma agentic de engenharia de software completa** da OpenAI, composta por CLI de terminal, Desktop App, Goal Mode de longa duração, Computer Use nativo e módulo de segurança dedicado (Codex Security).

## Visão Geral
O **OpenAI Codex** é a solução oficial da OpenAI para engenharia de software autônoma e assistida, equipada com modelos de raciocínio avançado (como **GPT-5.5** e variantes de reasoning). A plataforma opera tanto no terminal nativo quanto em aplicação desktop, superando limitações de "single-turn" para executar tarefas completas de ciclo de vida de código: planejamento, edição multi-arquivo, execução de testes, commits e resolução de segurança.

## Principais Funcionalidades e Novidades (2025–2026)
- **Interfaces Disponíveis:**
  - **Codex CLI (`@openai/codex`):** Agente de linha de comando que lê a estrutura do repositório, aplica modificações diretamente no código, roda suítes de testes e prepara commits.
  - **Codex Desktop App:** Aplicação desktop (macOS e Windows) desenhada como centro de comando com visualização gráfica de sessões paralelas, histórico de tarefas e árvore de arquivos.
- **Autonomia com Goal Mode:** O agente opera orientado a metas complexas ao longo de horas, mantendo estado persistente entre turnos e auto-corrigindo regressões sem necessidade de prompts constantes.
- **Computer Use & Appshots:**
  - **Computer Use:** Habilidade de interagir com aplicações e janelas gráficas locais (cliques, digitação e inspeção visual).
  - **Appshots:** Captura automática do contexto visual de janelas ativas para diagnosticar problemas visuais de UI/UX ou acompanhar execuções.
- **Codex Security:** Módulo dedicado que realiza modelagem de ameaças (*threat modeling*), varredura estática e dinâmica de vulnerabilidades (SAST/DAST) e sintetiza patches de correção em contêineres sandbox isolados.
- **Ecossistema e Extensibilidade:**
  - **Suporte MCP (Model Context Protocol):** Integração com servidores MCP locais e remotos para consumo de ferramentas padronizadas.
  - **Plugins de Toolchain:** Conexões com serviços como Sentry, Datadog e Linear para captura de incidentes e abertura de correções automatizadas.
  - **Triggers do GitHub:** Disparo de execuções automatizadas em resposta a pull requests, issues e pushes de código.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Raciocínio Profundo de Modelos de Fronteira:** Alta taxa de sucesso na resolução de problemas lógicos e arquiteturais difíceis.
- **Segurança Nativa e Sandboxing:** Isolamento robusto de execução via containers (bubblewrap/Docker), prevenindo efeitos colaterais na máquina host.
- **Operação Multi-Superfície:** Transição natural entre terminal ágil e aplicativo desktop visual.

### Limitações
- **Dependência do Ecossistema OpenAI:** Restrito aos modelos da OpenAI, sem opção de roteamento direto para modelos de terceiros (Anthropic, Gemini ou open-weights).
- **Custo Operacional sob Demanda:** Tarefas extensas em Goal Mode com reasoning avançado consomem volume significativo de tokens de API.

## Casos de Uso
- Resolução ponta a ponta de bugs complexos e desenvolvimento de novas funcionalidades com Goal Mode.
- Auditorias contínuas de segurança e correção autônoma de vulnerabilidades via Codex Security.
- Interações com sistemas e testes de interfaces visuais usando Computer Use e Appshots.
- Automação DevOps e administração de sistemas com tradução contextual de linguagem natural para shell.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário (OpenAI).
- **Preço:** Requer chave de API da OpenAI (cobrança por tokens de entrada/saída/reasoning) ou acesso via assinaturas empresariais (ChatGPT Pro, Team ou Enterprise com cotas integradas).
- **Agnóstico de Provedor:** Não (exclusivo para modelos OpenAI).

## Links Úteis
- **Site Oficial:** [https://openai.com/index/openai-codex/](https://openai.com/index/openai-codex/)
- **Pacote NPM:** [https://www.npmjs.com/package/@openai/codex](https://www.npmjs.com/package/@openai/codex)
- **GitHub Copilot CLI:** [https://docs.github.com/en/copilot/github-copilot-in-the-cli](https://docs.github.com/en/copilot/github-copilot-in-the-cli)
