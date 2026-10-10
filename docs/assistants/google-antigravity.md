# Google Antigravity

> [!NOTE]
> O Google Antigravity representa a consolidação do paradigma **agent-first**: um ecossistema completo em contínua evolução (plataforma Antigravity 2.0, IDE customizada, CLI `agy`, Gemini CLI open-source e SDK em Python) impulsionado pelos modelos **Gemini 2.5 Pro** e **Gemini 2.5 Flash**, com profunda integração ao Google AI Studio e Vertex AI, onde a IA atua como parceiro autônomo com subagentes paralelos e artefatos verificáveis.

## Visão Geral
O **Google Antigravity** é a plataforma de engenharia de software agentic desenvolvida pela equipe do **Google DeepMind**. Concebida para operar com os modelos mais avançados da família Gemini — com destaque para o **Gemini 2.5 Pro** e o **Gemini 2.5 Flash**, que trazem saltos expressivos em raciocínio lógico, planejamento arquitetural e geração precisa de código, além das séries Gemini 3, 3.5 e 3.8 Flash/Pro —, a ferramenta ultrapassa o modelo de autocompletar convencional ao atuar como um centro de operações (*home base*) para gerenciar, planejar e executar fluxos de desenvolvimento complexos e assíncronos de ponta a ponta.

## Principais Funcionalidades e Novidades (2025–2026)
- **Ecossistema Multi-Formato e Evolução Contínua (Antigravity 2.0):**
  - **Ambiente Standalone (Desktop App):** Central de controle independente para macOS, Windows e Linux, permitindo gerenciar múltiplos repositórios e acompanhar sessões paralelas de agentes desacopladas da janela de edição.
  - **Editor View (IDE Integrada):** Fork adaptado do VS Code voltado para pair programming síncrono, diffs interativos e chat contextual.
  - **Antigravity CLI (`agy`):** Interface de linha de comando leve para automações locais de shell, scripts e esteiras de CI/CD.
  - **Gemini CLI (Open-Source - Apache 2.0):** Lançamento da interface de linha de comando oficial de código aberto sob licença Apache 2.0, levando recursos e autonomia de agentes diretamente para o terminal do desenvolvedor.
  - **Antigravity Python SDK:** Biblioteca programática para orquestrar agentes e integrar capacidades do Antigravity em pipelines internos de engenharia.
  - **Evolução Contínua da Plataforma Antigravity 2.0:** Otimizações contínuas de estabilidade, sincronização fluida entre terminal, editor e app desktop, além de melhor suporte para grandes monorepos.
- **Modelos Gemini de Última Geração (Gemini 2.5 Pro & Gemini 2.5 Flash):**
  - Integração nativa dos modelos Gemini 2.5 Pro e Flash, proporcionando tempos de resposta otimizados, menor latência e raciocínio aprofundado para análise e modificação de bases de código complexas.
- **Integração Profunda com Google AI Studio e Vertex AI:**
  - Fluxo integrado que permite prototipar e validar agentes e prompts no **Google AI Studio** e promovê-los com facilidade para ambientes de produção no **Google Cloud Vertex AI**, atendendo a requisitos corporativos de segurança, governança, chaves gerenciadas e conformidade.
- **Orquestração de Subagentes Dinâmicos:**
  - Instanciação de subagentes especializados sob demanda (ex: subagente de pesquisa no código, subagente de execução de testes, subagente de documentação), rodando em paralelo sem poluir a sessão principal.
- **Planning Mode Estruturado:**
  - Criação automática de planos de arquitetura e implementação (`implementation_plan.md`) com parada mandatória para revisão e aprovação humana antes de executar alterações no código.
- **Scheduled Tasks (`/schedule`):**
  - Agendador integrado de tarefas com suporte a expressões cron e temporizadores de disparo único (*one-shot*), viabilizando verificações periódicas de dependências, checagens de liveness e auditorias noturnas.
- **Navegador Embutido & Generative UI:**
  - Subagente de browser com automação Playwright/Chrome para coletar documentações em tempo real, interagir com aplicações locais e validar fluxos E2E. Capacidade de renderizar widgets interativos e interfaces visuais diretamente no chat.
- **Segurança, Sandboxing e JSON Hooks:**
  - Execução segura em sandbox restrito por padrão (bloqueio de rede e contenção de arquivos), com suporte a bypass granular aprovado pelo usuário.
  - Guardrails configuráveis via JSON Hooks para interceptação e validação de comandos sensíveis.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Rigor e Confiabilidade (Trust Gap Reduction):** O uso de artefatos estruturados e modo de planejamento reduz alucinações e garante previsibilidade de alterações em bases grandes.
- **Flexibilidade de Modelos e Raciocínio de Ponta:** Otimizado nativamente para a família Gemini (incluindo Gemini 2.5 Pro e Flash para raciocínio analítico e geração rápida), com suporte a modelos externos integrados de alta capacidade.
- **Orquestração Multi-Agente Completa:** Capacidade de orquestrar subagentes em paralelo com isolamento de contexto e canais de mensageria dedicados.
- **Abertura e Integração Empresarial:** Disponibilização do Gemini CLI como código aberto (Apache 2.0) aliada ao poder corporativo do Vertex AI e flexibilidade do Google AI Studio.

### Limitações
- **Curva de Adoção para Projetos Triviais:** O overhead do planejamento estruturado pode ser desnecessário para alterações pontuais de uma linha.
- **Ecossistema de Configurações:** Requer familiaridade com a gestão de permissões de sandbox e regras de projeto (.gemini/rules e skills).

## Casos de Uso
- Engenharia de software autônoma de ponta a ponta (do planejamento arquitetural aos testes E2E).
- Refatorações em larga escala com múltiplos subagentes dividindo responsabilidades entre módulos.
- Diagnóstico interativo de builds quebrados com testes em navegador real e inspeção de console.
- Automação via terminal com Gemini CLI e agendamento de rotinas de manutenção de código via Scheduled Tasks.
- Implementação de fluxos de IA em larga escala integrados a pipelines corporativos no Vertex AI.

## Status, Preço e Licenciamento
- **Modelo:** Híbrido — Plataforma e editor proprietários (Google DeepMind) com componentes de código aberto, como o **Gemini CLI** (licença Apache 2.0).
- **Preço:** Disponível em preview público com cota gratuita para avaliação individual via Google AI Studio; governança, cotas dedicadas e conformidade corporativa via Vertex AI e Gemini Enterprise Platform.
- **Agnóstico de Provedor:** Otimizado prioritariamente para o ecossistema Gemini, com flexibilidade multi-modelo em fluxos avançados.

## Links Úteis
- **Site Oficial:** [https://antigravity.google](https://antigravity.google)
- **Google DeepMind:** [https://deepmind.google/](https://deepmind.google/)
- **Google AI Studio:** [https://aistudio.google.com/](https://aistudio.google.com/)
- **Google Cloud Vertex AI:** [https://cloud.google.com/vertex-ai](https://cloud.google.com/vertex-ai)
