# Hermes (Nous Research)

> [!NOTE]
> O Hermes destaca-se como um **agente auto-evolutivo**: ele sintetiza fluxos bem-sucedidos em "Skills" em Markdown e as refina autonomamente via DSPy e otimização evolutiva (GEPA), tornando-se mais rápido e preciso a cada execução. A partir da versão **v0.16+** (outubro de 2026), atinge execução 60% mais veloz, mais de 100 skills integradas, melhor gerenciamento de memória em sessões longas e suporte aos modelos mais recentes, incluindo Claude 4.5 Sonnet e GPT-5.5.

## Visão Geral
O **Hermes** (desenvolvido pela **Nous Research**, pacote `hermes-agent`) é um agente autônomo open-source concebido como um assistente pessoal persistente voltado a desenvolvedores e operadores de infraestrutura. Operando nativamente no terminal e integrável a múltiplos canais de mensageria, o Hermes combina execução local de comandos com um loop contínuo de aprendizado, auto-geração de skills e exportação de trajetórias para fine-tuning. Com as atualizações contínuas da versão **v0.16+**, o agente expandiu sua compatibilidade para suportar os modelos de ponta mais recentes — incluindo **Claude 4.5 Sonnet**, **GPT-5.5**, **Llama 3.3** e **Mistral Large** (via Ollama) —, além de aprimorar a gestão de memória para sessões de longa duração.

## Principais Funcionalidades e Novidades (2025–2026)
- **Sistema de Skills e Aprendizado Auto-Evolutivo:**
  - **Criação e Refinamento de Skills:** Converte resoluções bem-sucedidas em arquivos estruturados em `~/.hermes/skills/`, consultando-os para acelerar problemas futuros.
  - **100+ Skills Pré-instaladas:** Pacote bundled expandido com mais de 100 skills integradas (anteriormente 90+), com novas categorias dedicadas para DevOps e infraestrutura em nuvem (AWS, GCP, Azure CLI) e ferramentas de monitoramento e observabilidade (Grafana, Prometheus), além de MLOps (`dspy`, `serving-llms-vllm`, `weights-and-biases`), automação de código (`github-pr-workflow`, `github-code-review`) e produtividade.
  - **Auto-Evolução com DSPy e GEPA:** Mecanismo experimental que utiliza algoritmos genéticos e compilação de prompts para reescrever e otimizar as próprias skills a partir de traces de execução.
  - **Hub Comunitário:** Download e compartilhamento de skills via `agentskills.io`.
- **Orquestração Multi-Agente via Kanban Durável:**
  - **Melhorias no Kanban (v0.16+):** Sistema de delegação de tarefas estilo Kanban com priorização automática de tarefas (*automatic task prioritization*), monitoramento de batimentos cardíacos (*heartbeats*), detecção e recuperação aprimorada de agentes zumbis (*zombie agent detection and recovery*) e re-tentativas automáticas contra alucinações.
- **Automação de Computador e Navegador (Computer Use):**
  - Driver universal de Computer Use compatível com múltiplos provedores de visão para capturas de tela e interação com interfaces de desktop.
  - Automação completa de browser via Playwright/Chromium para extração de dados e auditoria de aplicações web.
- **MLOps e Geração de Dados de Treinamento:**
  - **Batch Processing:** Geração de milhares de trajetórias de chamadas de ferramentas em lote com checkpoints persistentes.
  - **Exportação de Trajetórias:** Exportação nativa em formatos compatíveis com ShareGPT para fine-tuning e integração com frameworks de Reinforcement Learning (ex: Atropos).
- **Gateway Multicanal Unificado:**
  - Suporte simultâneo a mais de 5 plataformas (Telegram, Slack, Discord, WhatsApp e Signal) em um único processo gateway, com suporte móvel (Android via Termux) e agendador cron integrado.
- **Performance, Hot-path e Gestão de Memória:**
  - **Loop de Execução 60% Mais Veloz:** O loop de execução do agente opera agora **60% mais rápido** em relação à versão inicial (evoluindo dos 47% alcançados nas versões v0.14/v0.15), com inicialização instantânea via `uv` e diagnósticos LSP integrados em tempo real.
  - **Gerenciamento Avançado de Memória:** Subsistema otimizado de gestão de contexto e retenção de estado para sessões longas (*long sessions*), prevenindo degradação de resposta e saturação de tokens ao longo de fluxos complexos.
- **Suporte Expandido a Modelos de Ponta:**
  - Compatibilidade nativa com os mais recentes LLMs do mercado, incluindo **Claude 4.5 Sonnet**, **GPT-5.5**, **Llama 3.3** e **Mistral Large** (executado localmente via Ollama), garantindo total liberdade de escolha de inferência.
- **Anúncio do Hermes Pro:**
  - Versão comercial anunciada pela Nous Research voltada ao público corporativo, com lançamento planejado trazendo suporte profissional dedicado e recursos avançados para times (*team features*).

## Pontos Fortes e Limitações
### Pontos Fortes
- **Auto-Aperfeiçoamento Contínuo:** Acúmulo progressivo de conhecimento prático por meio do ecossistema de skills.
- **Privacidade e Self-Hosting:** Capacidade de operar de forma 100% privada com modelos locais (vLLM, Ollama com Llama 3.3 e Mistral Large) ou via nuvem com modelos de fronteira (Claude 4.5 Sonnet, GPT-5.5, OpenRouter).
- **Ecossistema Abrangente de DevOps e Nuvem:** Mais de 100 skills nativas com cobertura para AWS, GCP, Azure CLI, além de ferramentas de observabilidade como Grafana e Prometheus.
- **Alta Eficiência e Resiliência Operacional:** Loop 60% mais rápido que a versão inicial, gerenciamento refinado de memória para sessões longas e orquestração Kanban com recuperação automática de agentes zumbis.
- **Multicanalidade Extrema:** Acesso e controle de fluxos de engenharia diretamente pelo smartphone via mensageiros.

### Limitações
- **Configuração Técnica:** Demanda maior familiaridade com terminal, variáveis de ambiente e gerenciamento de modelos.
- **Foco Primário em Backend/DevOps:** Menos direcionado a preview visual interativo de UI comparado a IDEs dedicadas.

## Casos de Uso
- Administração remota de servidores e automação de infraestrutura em nuvem e observabilidade (AWS, GCP, Azure, Grafana, Prometheus) via bots de mensageria.
- Geração de datasets sintéticos de trajetórias de agentes para pipelines de fine-tuning e RL.
- Execução de tarefas longas de desenvolvimento com supervisão assíncrona no Kanban durável, priorização automatizada e recuperação contra travamentos.
- Automação de engenharia com modelos de última geração (Claude 4.5 Sonnet, GPT-5.5, Llama 3.3 e Mistral Large).

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Nous Research) com edição comercial planejada (**Hermes Pro**).
- **Preço:**
  - **Hermes Agent (Community):** Gratuito (código aberto). O usuário fornece infraestrutura própria e chaves de API/modelos locais.
  - **Hermes Pro (Anunciado):** Versão comercial planejada com suporte profissional dedicado e recursos avançados para times (*team features*).
- **Agnóstico de Provedor:** Sim (suporta OpenRouter, OpenAI, Anthropic, Google, vLLM e Ollama, incluindo Claude 4.5 Sonnet, GPT-5.5, Llama 3.3 e Mistral Large).

> [!NOTE]
> O anúncio do **Hermes Pro** marca a expansão do ecossistema para ambientes corporativos, complementando a base de código aberto com suporte comercial e recursos colaborativos de equipe.

## Links Úteis
- **Site Oficial:** [https://nousresearch.com/](https://nousresearch.com/)
- **Repositório Oficial (GitHub):** [https://github.com/NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
- **Hub de Skills:** [https://agentskills.io/](https://agentskills.io/)
