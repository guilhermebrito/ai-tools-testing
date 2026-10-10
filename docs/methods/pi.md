# Pi (Earendil Works)

> [!NOTE]
> O Pi consolidou sua migração para o escopo comunitário **`@earendil-works`** (anteriormente `@mariozechner`) e evoluiu para a série **v0.80+**, trazendo atualizações incrementais focadas em estabilidade, recursos avançados de TUI (incluindo painéis em split-screen), novos provedores de inferência de ultra-baixa latência (Groq e Cerebras) e o anúncio do **Pi Studio (Preview)** para gerenciamento visual de agentes.

## Visão Geral
O **Pi** (mantido pela **Earendil Works**) é um framework e toolkit de linha de comando de código aberto, focado na construção de interfaces de agentes e ferramentas de desenvolvimento ricas para o terminal. Na série **v0.80+**, o Pi combina estabilidade aprimorada com suporte contínuo aos modelos mais avançados da indústria — como Claude 3.7 Sonnet, OpenAI o3-mini e GPT-4o, Google Gemini 2.5 Pro e Flash, além de modelos abertos como Llama 3.3 e DeepSeek V3 —, operando tanto via endpoints nativos e provedores de ultra-baixa latência (Groq e Cerebras) quanto em servidores locais. Destacando-se pelo módulo `coding-agent`, pela expansão da experiência TUI e pelo anúncio do **Pi Studio**, o projeto disponibiliza um ambiente unificado e extensível tanto para desenvolvedores hackers quanto para equipes corporativas.

## Principais Funcionalidades e Novidades (2025–2026 · v0.80+)
- **Estabilidade e Ciclo Incremental (v0.80+):**
  - Releases incrementais contínuos com foco primordial em estabilidade de execução, tratamento resiliente de streams de resposta e robustez durante sessões prolongadas de codificação.
- **Interface TUI Rica e Interativa:**
  - *Startup Header:* Cabeçalho dinâmico com resumo compacto de agentes, templates de prompt e extensões ativas (detalhes expandíveis via `Ctrl+O`).
  - *Indicadores de Progresso Configuráveis:* Feedback de status configurável via `ctx.ui.setWorkingIndicator()` com modos animado, estático ou oculto para extensões.
  - *Hiperlinks Clicáveis:* Renderização nativa de links Markdown como hiperlinks OSC 8 clicáveis em emuladores de terminal modernos.
  - *Temas e Customizações Visuais:* Novos temas nativos e opções aprimoradas de customização visual para componentes de interface no terminal.
  - *Painéis em Split-Screen:* Suporte a divisão de tela na TUI, permitindo monitorar e alternar entre múltiplas conversas e fluxos simultâneos de agentes no mesmo terminal.
- **Roteamento Inteligente e Suporte Multi-Modelo:**
  - API unificada e agnóstica para **OpenAI**, **Anthropic**, **Google**, **Together AI**, **vLLM**, **Ollama**, **OpenRouter**, **Groq** e **Cerebras**.
  - *Novos Provedores de Altíssima Velocidade:* Integração nativa e otimizada com endpoints de inferência acelerada por hardware de **Groq** e **Cerebras**, viabilizando tempos de resposta mínimos.
  - *Fallback Aprimorado via OpenRouter:* Roteamento inteligente com resiliência otimizada e estratégias de fallback automático no OpenRouter para contornar instabilidades ou limites de taxa (rate limits).
  - Configuração de roteamento via `models.json` com fallback automático, seleção por restrições de custo e latência.
  - Geração de imagens e suporte a modelos multimodais de visão diretamente pela linha de comando.
- **Extensibilidade e Hooks Avançados:**
  - *Novos Lifecycle Hooks (`on_session_start` e `on_session_end`):* Ganchos de ciclo de vida dedicados para gerenciar o estado da sessão, permitindo injeção de contexto na inicialização e rotinas estruturadas de persistência ou teardown no encerramento.
  - *Lifecycle Hook `after_provider_response`:* Auditoria de headers HTTP, telemetria de latência e inspeção de tokens antes da decodificação do stream.
  - *Documentação e Exemplos de Extensões:* Guias e documentação aprofundada com novos repositórios de exemplos práticos para criação, testes e integração de extensões personalizadas.
  - *Prompt Templates:* Validação enriquecida com `argument-hint` para autocompletar dinâmico em templates customizados.
  - *Session Branching:* Comando `/clone` para criar forks de sessões ativas e explorar refatorações alternativas em ramificações separadas.
- **Pi Studio (Preview):**
  - Anúncio de uma interface web complementar para gerenciamento e configuração visual de agentes, permitindo inspecionar parâmetros, fluxos e execuções fora do terminal.
- **ChatOps e Portabilidade Multiplataforma:**
  - Utilitários prontos para criação e hospedagem de bots de Slack e Discord conectados aos agentes locais.
  - Binários e pacotes compilados para macOS, Linux e **Windows ARM64** com artefatos standalone.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Máxima Hackabilidade:** Estrutura altamente modular onde cada ferramenta, prompt e componente visual de TUI pode ser sobrescrito pelo desenvolvedor.
- **Independência de Nuvens Proprietárias:** Ideal para execução em clusters locais com vLLM sem depender de interfaces web de terceiros.
- **Interface de Terminal Sofisticada e Flexível:** Entrega uma experiência visual rica no terminal com novos temas e suporte a split-screen, preservando agilidade e baixo consumo de recursos.
- **Latência Minimizada:** Conexão nativa com provedores de inferência ultra-rápidos como Groq e Cerebras, acelerando a interação e o ciclo de feedback.

### Limitações
- **Não é uma Aplicação "Plug-and-Play":** Exige entendimento de código e configuração por parte do desenvolvedor para montar o ecossistema ideal (embora a introdução do Pi Studio vise reduzir essa barreira).
- **Ecossistema em Expansão:** Menor quantidade de extensões prontas comerciais quando comparado ao ecossistema do VS Code.

## Casos de Uso
- Equipes de engenharia operando instâncias internas de vLLM ou Ollama e buscando interfaces de chat/revisão locais customizadas.
- Condução e monitoramento simultâneo de múltiplos fluxos de agentes em paralelo via painéis split-screen no terminal.
- Automação de ChatOps conectando bots de Slack/Discord à base de código com segurança on-premise.
- Criação de CLIs e assistentes de engenharia customizados para ferramentas internas de empresas com extensões sob medida.
- Aplicações sensíveis à latência utilizando pipelines de resposta ultra-rápidos com Groq e Cerebras.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT).
- **Preço:** Totalmente gratuito e aberto (ecossistema CLI/TUI e preview do Pi Studio).
- **Agnóstico de Provedor:** Sim (100% agnóstico — suportando OpenAI, Anthropic, Google, Groq, Cerebras, Together AI, vLLM, Ollama e OpenRouter).

## Links Úteis
- **Site Oficial:** [https://pi.dev/](https://pi.dev/)
- **Repositório Oficial (GitHub):** [https://github.com/earendil-works/pi](https://github.com/earendil-works/pi)
- **Pacote NPM:** [https://www.npmjs.com/package/@earendil-works/pi-coding-agent](https://www.npmjs.com/package/@earendil-works/pi-coding-agent)
