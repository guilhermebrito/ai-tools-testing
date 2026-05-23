# Hermes (Nous Research)

> [!NOTE]
> O Hermes é um agente **auto-evolutivo**: ele resolve problemas, cria "Skills" documentadas sobre como resolvê-los, e as refina automaticamente ao longo do tempo — ficando mais rápido e preciso a cada tarefa.

## Visão Geral
Desenvolvido pela **Nous Research**, o **Hermes** é um agente de IA open-source altamente capaz, desenhado para atuar como um **assistente pessoal persistente** focado em desenvolvedores. Instalável via `pip install hermes-agent`, ele opera como um orquestrador de terminal com loop de aprendizado contínuo e suporte a mais de **20 plataformas de mensageria**.

---

## Funcionalidades e Recursos (2026)

### Sistema de Skills (Auto-Aperfeiçoamento)
*   **Criação de Skills:** Quando resolve um problema complexo, o Hermes escreve uma "Skill" (documento Markdown) detalhando a solução. No futuro, consulta essas skills para resolver problemas similares de forma mais rápida e precisa.
*   **Auto-Evolução (Experimental):** Recursos como `hermes-agent-self-evolution` utilizam DSPy e GEPA para **reescrever e otimizar automaticamente** os arquivos de skills com base em traces de execução.

### Orquestração Multi-Agente (Kanban)
*   **Kanban Board Durável:** Sistema de delegação de tarefas para times de agentes com monitoramento por heartbeat, detecção de tarefas "zumbi", retries automáticos e recuperação de alucinações.

### Automação e Computer Use
*   **Computer Use Universal:** Driver de interação com a interface gráfica (screenshots, cliques, inputs de teclado) compatível com múltiplos modelos, não limitado a provedores específicos.
*   **Tool Gateway:** Gateway integrado para web search (Brave, DuckDuckGo, Exa, Tavily), geração de imagens, text-to-speech e automação avançada de navegador.

### Conectividade
*   **20+ Plataformas de Mensageria:** Telegram, Discord, Slack, WhatsApp, Signal, Microsoft Teams, Google Chat, LINE e SimpleX Chat — tudo a partir de um único processo gateway.
*   **Suporte Mobile:** Operação nativa em Android via Termux.
*   **Session Handoff:** Transferência de sessões ativas entre plataformas de forma transparente.

### Performance (v0.14.0+)
*   **Agent Loop 47% mais rápido:** Otimizações no hot-path de execução.
*   **Cold Start -19s:** Redução significativa no tempo de inicialização.
*   **LSP Diagnostics:** Erros de language server em tempo real diretamente no workspace do agente.
*   **Instalação Nativa Windows:** Sem necessidade de WSL2.

---

## Pontos Fortes
*   **Privacidade e Self-Hosting:** Roda inteiramente em infraestrutura própria, ideal para código sensível.
*   **Agnóstico de Modelo:** Suporta centenas de modelos — OpenAI, Anthropic, xAI Grok, Google Gemini, Ollama, LM Studio e outros — sem alteração de código.
*   **Aprendizado Contínuo:** O loop fechado de Skills garante melhoria progressiva com o uso.
*   **Alcance Multi-Plataforma:** A capacidade de receber comandos via Telegram ou WhatsApp e executar deploys torna-o um assistente verdadeiramente ubíquo.

---

## Casos de Uso
*   Assistente pessoal permanente rodando em VPS privada ou máquina local.
*   Automação de CI/CD não-padrão e tarefas de infraestrutura.
*   Delegação de tarefas complexas e longas a partir de dispositivos móveis via chat (Telegram/WhatsApp).
*   Orquestração de times de agentes via Kanban para projetos de larga escala.

---

## Links Úteis
*   **Nous Research:** [https://nousresearch.com/](https://nousresearch.com/)
*   **Repositório Oficial (GitHub):** [https://github.com/NousResearch/Hermes](https://github.com/NousResearch/Hermes)
