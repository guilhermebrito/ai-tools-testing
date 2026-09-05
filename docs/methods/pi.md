# Pi (Earendil Works)

> [!NOTE]
> O Pi migrou oficialmente para o escopo comunitário **`@earendil-works`** (anteriormente `@mariozechner`), consolidando-se como um toolkit open-source ultracustomizável para criação de agentes com TUI rica de terminal e suporte multi-provedor avançado.

## Visão Geral
O **Pi** (mantido pela **Earendil Works**) é um framework e toolkit de linha de comando de código aberto, focado na construção de interfaces de agentes e ferramentas de desenvolvimento ricas para o terminal. Destacando-se pelo módulo `coding-agent`, o Pi disponibiliza uma interface visual em terminal (TUI) personalizável e uma camada de abstração de IA unificada para ambientes corporativos e desenvolvedores hackers.

## Principais Funcionalidades e Novidades (2025–2026 · v0.74+)
- **Interface TUI Rica e Interativa:**
  - *Startup Header:* Cabeçalho dinâmico com resumo compacto de agentes, templates de prompt e extensões ativas (detalhes expandíveis via `Ctrl+O`).
  - *Indicadores de Progresso Configuráveis:* Feedback de status configurável via `ctx.ui.setWorkingIndicator()` com modos animado, estático ou oculto para extensões.
  - *Hiperlinks Clicáveis:* Renderização nativa de links Markdown como hiperlinks OSC 8 clicáveis em emuladores de terminal modernos.
- **Roteamento Inteligente e Suporte Multi-Modelo:**
  - API unificada e agnóstica para **OpenAI**, **Anthropic**, **Google**, **Together AI**, **vLLM**, **Ollama** e **OpenRouter**.
  - Configuração de roteamento via `models.json` com fallback automático, seleção por restrições de custo e latência.
  - Geração de imagens e suporte a modelos multimodais de visão diretamente pela linha de comando.
- **Extensibilidade e Hooks Avançados:**
  - *Lifecycle Hooks:* Hook `after_provider_response` para auditoria de headers HTTP, telemetria de latência e inspeção de tokens antes da decodificação do stream.
  - *Prompt Templates:* Validação enriquecida com `argument-hint` para autocompletar dinâmico em templates customizados.
  - *Session Branching:* Comando `/clone` para criar forks de sessões ativas e explorar refatorações alternativas em ramificações separadas.
- **ChatOps e Portabilidade Multiplataforma:**
  - Utilitários prontos para criação e hospedagem de bots de Slack e Discord conectados aos agentes locais.
  - Binários e pacotes compilados para macOS, Linux e **Windows ARM64** com artefatos standalone.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Máxima Hackabilidade:** Estrutura altamente modular onde cada ferramenta, prompt e componente visual de TUI pode ser sobrescrito pelo desenvolvedor.
- **Independência de Nuvens Proprietárias:** Ideal para execução em clusters locais com vLLM sem depender de interfaces web de terceiros.
- **Interface de Terminal Sofisticada:** Entrega uma experiência visual rica preservando a agilidade e o baixo consumo de recursos do terminal.

### Limitações
- **Não é uma Aplicação "Plug-and-Play":** Exige entendimento de código e configuração por parte do desenvolvedor para montar o ecossistema ideal.
- **Ecossistema em Expansão:** Menor quantidade de extensões prontas comerciais quando comparado ao ecossistema do VS Code.

## Casos de Uso
- Equipes de engenharia operando instâncias internas de vLLM ou Ollama e buscando interfaces de chat/revisão locais customizadas.
- Automação de ChatOps conectando bots de Slack/Discord à base de código com segurança on-premise.
- Criação de CLIs e assistentes de engenharia customizados para ferramentas internas de empresas.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT).
- **Preço:** Totalmente gratuito e aberto.
- **Agnóstico de Provedor:** Sim (100% agnóstico).

## Links Úteis
- **Site Oficial:** [https://pi.dev/](https://pi.dev/)
- **Repositório Oficial (GitHub):** [https://github.com/earendil-works/pi](https://github.com/earendil-works/pi)
