# OpenHands

> [!NOTE]
> O OpenHands (anteriormente OpenDevin) é o principal projeto open-source de engenheiros de software de IA autônomos, mantendo uma comunidade vibrante com mais de **70.000 stars no GitHub** e contribuidores ativos. Apresenta desempenho líder no benchmark **SWE-bench**, suporte aos modelos mais recentes (como Claude 4.5 Sonnet, GPT-5.5 e Gemini), automação com o **GitHub Resolver**, ciclo rápido de lançamentos a partir da versão **0.40+**, ecossistema com o **Agent Control Plane** e a oferta gerenciada **OpenHands Cloud**.

## Visão Geral
O **OpenHands** (mantido pela **All-Hands-AI**) é uma plataforma aberta para a criação e execução de agentes autônomos de engenharia de software, atualmente na **versão 0.40+** com ciclo de lançamento ágil e contínuo. Capaz de atuar como um desenvolvedor parceiro ou individual, o agente navega autonomamente por repositórios, elabora planos formais, escreve código, executa compilações e testes em terminais isolados e resolve falhas de ponta a ponta.

Destaca-se como um dos agentes open-source de melhor desempenho no benchmark **SWE-bench**, combinando arquitetura robusta de ferramentas com suporte expandido aos modelos de ponta mais recentes, incluindo **Claude 4.5 Sonnet**, **GPT-5.5** e as últimas versões do **Gemini**.

## Principais Funcionalidades e Novidades (2025–2026)
- **Desempenho de Ponta no SWE-bench:**
  - Reconhecido como um dos agentes de código aberto com maior pontuação e eficácia no benchmark **SWE-bench**, solucionando problemas reais de engenharia de software e bugs complexos com alta taxa de acerto por meio de técnicas avançadas de scaffold e inferência.
- **GitHub Resolver (Resolução Automática de Issues):**
  - O **OpenHands Resolver** atua na resolução automatizada de *issues* do GitHub (via execução local ou integrado a GitHub Actions), analisando o problema, criando a solução, executando a bateria de testes e abrindo Pull Requests completos e prontos para revisão.
- **Versão 0.40+ e Ciclo Rápido de Releases:**
  - Evolução contínua a partir da versão **0.40+**, mantendo um ritmo acelerado de lançamentos frequentes com aprimoramentos de runtime, gestão de contexto, ferramentas e estabilidade geral.
- **OpenHands Cloud em Constante Evolução:**
  - A plataforma gerenciada SaaS continua evoluindo para simplificar a adoção corporativa, fornecendo ambientes pré-configurados em nuvem sem a necessidade de gerenciar infraestrutura própria de containers ou clusters.
- **Comunidade Crescente (70k+ Stars):**
  - Ecossistema consolidado com mais de **70.000 stars no GitHub** e uma ampla comunidade de contribuidores ativos, impulsionando extensões, correções ágeis e integrações contínuas.
- **Suporte Expandido a Modelos de Ponta:**
  - Compatibilidade imediata com as famílias de modelos mais recentes, incluindo **Claude 4.5 Sonnet**, **GPT-5.5** e os novos lançamentos da linha **Gemini**, além de modelos locais via Ollama/vLLM.
- **Agent Control Plane (Plano de Controle Empresarial):**
  - Camada de gerenciamento centralizado para orquestrar frotas inteiras de agentes de software simultaneamente, com telemetria unificada, métricas de resolução e auditoria descrita como "o Kubernetes para agentes de IA".
- **Planning Mode Estruturado:**
  - O agente mapeia dependências e cria um arquivo de especificação estruturado (`PLAN.md`) antes de tocar no código-fonte, submetendo o plano à revisão humana para validação do escopo e arquitetura.
- **Aceleração com KVM e Sandboxing Isolado:**
  - **KVM Acceleration (`SANDBOX_KVM_ENABLED`):** Ambientes de execução de sandbox acelerados por virtualização KVM direta, reduzindo tempos de compilação e teste em comparação a containers emulados tradicionais.
  - **Isolamento Robusto:** Suporte nativo a Docker e clusters **Kubernetes**, garantindo segurança absoluta contra códigos maliciosos ou dependências corrompidas.
- **Navegação Web e Visual Inspection:**
  - Instanciação de navegadores virtuais para pesquisar documentações técnicas, consultar APIs externas e validar visualmente interfaces frontend construídas pelo agente.
- **Interface Gráfica e Usabilidade:**
  - Menu de comandos rápidos (*Slash Menu* `/`) na interface web para acionamento imediato de skills e ferramentas.
  - Suporte tanto a instâncias locais autogerenciadas (*Self-Hosted*) quanto ao serviço totalmente gerenciado **OpenHands Cloud (SaaS)**.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Totalmente Agnóstico e Sem Lock-in:** Suporte irrestrito e atualizado aos principais modelos do mercado (Claude 4.5 Sonnet, GPT-5.5, Gemini, DeepSeek e modelos locais via Ollama/vLLM).
- **Liderança em Benchmarks Open-Source:** Resultados comprovados de alta performance no benchmark SWE-bench.
- **Transparência e Auditabilidade:** Código 100% open-source sob licença permissiva MIT com comunidade vibrante (70k+ stars).
- **Prontidão Enterprise:** Arquitetura desenhada para execução em nuvem e clusters corporativos (KVM, Kubernetes, Agent Control Plane e OpenHands Cloud).

### Limitações
- **Consumo de Hardware e Tokens:** Ambientes complexos com múltiplos ciclos de tentativa-e-erro em compilações pesadas demandam alto uso computacional e de tokens.
- **Configuração de Sandbox:** Setup inicial com Docker ou Kubernetes pode exigir esforço de infraestrutura em ambientes corporativos com restrições severas de rede (amenizado com o OpenHands Cloud).

## Casos de Uso
- Resolução autônoma de *issues* e bugs no GitHub/GitLab com o **GitHub Resolver**, com submissão direta de Pull Requests prontos e validados.
- Modernização, migração de frameworks e refatoração de bases de código legadas em grande escala.
- Prototipagem acelerada de microsserviços e aplicações web completas.
- Operações de engenharia gerenciadas em larga escala via Agent Control Plane e OpenHands Cloud.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT) e versão gerenciada (OpenHands Cloud).
- **Preço:** Gratuito em modo Self-Hosted (o usuário provê chaves de API ou modelos locais); planos sob demanda no OpenHands Cloud (SaaS gerenciado).
- **Agnóstico de Provedor:** Sim (100% agnóstico).

## Links Úteis
- **Site Oficial:** [https://www.all-hands.dev/](https://www.all-hands.dev/)
- **Repositório Oficial (GitHub):** [https://github.com/All-Hands-AI/OpenHands](https://github.com/All-Hands-AI/OpenHands)
- **Documentação Oficial:** [https://docs.all-hands.dev/](https://docs.all-hands.dev/)
- **OpenHands Cloud:** [https://openhands.dev/](https://openhands.dev/)
