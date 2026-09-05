# Hermes (Nous Research)

> [!NOTE]
> O Hermes destaca-se como um **agente auto-evolutivo**: ele sintetiza fluxos bem-sucedidos em "Skills" em Markdown e as refina autonomamente via DSPy e otimização evolutiva (GEPA), tornando-se mais rápido e preciso a cada execução.

## Visão Geral
O **Hermes** (desenvolvido pela **Nous Research**, pacote `hermes-agent`) é um agente autônomo open-source concebido como um assistente pessoal persistente voltado a desenvolvedores e operadores de infraestrutura. Operando nativamente no terminal e integrável a múltiplos canais de mensageria, o Hermes combina execução local de comandos com um loop contínuo de aprendizado, auto-geração de skills e exportação de trajetórias para fine-tuning.

## Principais Funcionalidades e Novidades (2025–2026)
- **Sistema de Skills e Aprendizado Auto-Evolutivo:**
  - **Criação e Refinamento de Skills:** Converte resoluções bem-sucedidas em arquivos estruturados em `~/.hermes/skills/`, consultando-os para acelerar problemas futuros.
  - **90+ Skills Pré-instaladas:** Pacote bundled abrangendo MLOps (`dspy`, `serving-llms-vllm`, `weights-and-biases`), automação de código (`github-pr-workflow`, `github-code-review`) e produtividade.
  - **Auto-Evolução com DSPy e GEPA:** Mecanismo experimental que utiliza algoritmos genéticos e compilação de prompts para reescrever e otimizar as próprias skills a partir de traces de execução.
  - **Hub Comunitário:** Download e compartilhamento de skills via `agentskills.io`.
- **Orquestração Multi-Agente via Kanban Durável:**
  - Sistema de delegação de tarefas estilo Kanban com monitoramento de batimentos cardíacos (*heartbeats*), detecção de tarefas travadas e re-tentativas automáticas contra alucinações.
- **Automação de Computador e Navegador (Computer Use):**
  - Driver universal de Computer Use compatível com múltiplos provedores de visão para capturas de tela e interação com interfaces de desktop.
  - Automação completa de browser via Playwright/Chromium para extração de dados e auditoria de aplicações web.
- **MLOps e Geração de Dados de Treinamento:**
  - **Batch Processing:** Geração de milhares de trajetórias de chamadas de ferramentas em lote com checkpoints persistentes.
  - **Exportação de Trajetórias:** Exportação nativa em formatos compatíveis com ShareGPT para fine-tuning e integração com frameworks de Reinforcement Learning (ex: Atropos).
- **Gateway Multicanal Unificado:**
  - Suporte simultâneo a mais de 5 plataformas (Telegram, Slack, Discord, WhatsApp e Signal) em um único processo gateway, com suporte móvel (Android via Termux) e agendador cron integrado.
- **Performance e Hot-path:**
  - Loop de execução do agente 47% mais veloz a partir da v0.14/v0.15, inicialização instantânea via `uv` e diagnósticos LSP integrados em tempo real.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Auto-Aperfeiçoamento Contínuo:** Acúmulo progressivo de conhecimento prático por meio do ecossistema de skills.
- **Privacidade e Self-Hosting:** Capacidade de operar de forma 100% privada com modelos locais (vLLM, Ollama) ou via OpenRouter.
- **Multicanalidade Extrema:** Acesso e controle de fluxos de engenharia diretamente pelo smartphone via mensageiros.

### Limitações
- **Configuração Técnica:** Demanda maior familiaridade com terminal, variáveis de ambiente e gerenciamento de modelos.
- **Foco Primário em Backend/DevOps:** Menos direcionado a preview visual interativo de UI comparado a IDEs dedicadas.

## Casos de Uso
- Administração remota de servidores e automação de operações de infraestrutura via bots de mensageria.
- Geração de datasets sintéticos de trajetórias de agentes para pipelines de fine-tuning e RL.
- Execução de tarefas longas de desenvolvimento com supervisão assíncrona no Kanban durável.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Nous Research).
- **Preço:** Gratuito (código aberto). Usuário fornece infraestrutura própria e chaves de API/modelos locais.
- **Agnóstico de Provedor:** Sim (suporta OpenRouter, OpenAI, Anthropic, Google, vLLM e Ollama).

## Links Úteis
- **Site Oficial:** [https://nousresearch.com/](https://nousresearch.com/)
- **Repositório Oficial (GitHub):** [https://github.com/NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
- **Hub de Skills:** [https://agentskills.io/](https://agentskills.io/)
