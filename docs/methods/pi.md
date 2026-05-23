# Pi (Earendil Works)

> [!NOTE]
> O Pi migrou do escopo `@mariozechner` para `@earendil-works`, mas continua sendo um toolkit CLI open-source altamente hackável para criação de agentes de IA com TUI rica e suporte multi-provedor.

## Visão Geral
O **Pi** é um toolkit open-source mantido pela **Earendil Works** (anteriormente sob o namespace `@mariozechner`), voltado para a criação e interação com agentes de IA diretamente no terminal. O módulo `coding-agent` fornece uma interface TUI (Terminal User Interface) rica e uma API unificada para múltiplos provedores de modelos de linguagem.

---

## Funcionalidades Principais (2026 — v0.74.0+)

### Interface TUI (Terminal User Interface)
*   **Startup Header Interativo:** Resumo compacto dos agentes, templates e extensões carregados, com detalhes expandíveis via `Ctrl+O`.
*   **Working Indicators Configuráveis:** Extensões podem mostrar estados de trabalho animados, estáticos ou ocultos via `ctx.ui.setWorkingIndicator()`.
*   **Hyperlinks OSC 8:** Links em Markdown na saída do assistente renderizam como hyperlinks clicáveis em terminais compatíveis.

### Provedores e Modelos
*   **API Unificada:** Abstrai a complexidade de conexão com diferentes provedores: **OpenAI**, **Anthropic**, **Ollama**, **vLLM**, **Together AI** e **OpenRouter**.
*   **Geração de Imagens:** Suporte a APIs de geração de imagens, incluindo geração via OpenRouter.
*   **Roteamento OpenRouter:** Suporte completo a `models.json` com fallbacks, parâmetros de roteamento e restrições de custo/latência.

### Extensibilidade
*   **Hooks (`after_provider_response`):** Permitem que extensões inspecionem status HTTP e headers antes do consumo da stream.
*   **Prompt Templates com `argument-hint`:** Frontmatter aprimorado que fornece sugestões de autocomplete para templates de prompt.
*   **Sessões e Branching:** Comando `/clone` para duplicar a branch ativa em uma nova sessão, com APIs de extensão para lidar com forks.

### Integrações
*   **Slack Bots:** Suporte integrado para bots no Slack, facilitando o uso colaborativo do agente em times.
*   **Plataformas:** Suporte nativo para macOS, Linux e **Windows ARM64** (com artefatos standalone).

---

## Pontos Fortes
*   **Hackabilidade Extrema:** O toolkit mais customizável para desenvolvedores que querem construir sua própria plataforma de agentes.
*   **Foco em CLI:** Ferramentas de produtividade de terminal sem dependência de serviços web proprietários.
*   **Open Source (MIT):** Core MIT-licensed com planos para tiers comerciais futuros.

---

## Casos de Uso
*   Equipes que hospedam seus próprios pods de LLM (vLLM) e integram aos fluxos de CI/CD.
*   Criação de bots de desenvolvimento internos para Slack/Discord.
*   Desenvolvedores que desejam máximo controle sobre o runtime e a configuração de agentes.

---

## Migração de Namespace
> [!IMPORTANT]
> Os pacotes antigos sob `@mariozechner` foram deprecados. Novos installs devem usar o escopo `@earendil-works` (ex: `@earendil-works/pi-coding-agent`). Atualizações podem ser feitas via `pi update --self`.

---

## Links Úteis
*   **Site Oficial:** [https://pi.dev/](https://pi.dev/)
*   **Repositório Oficial (GitHub):** [https://github.com/earendil-works/pi](https://github.com/earendil-works/pi)
