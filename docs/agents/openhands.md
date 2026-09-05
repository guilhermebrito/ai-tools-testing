# OpenHands

> [!NOTE]
> O OpenHands (anteriormente OpenDevin) é o principal projeto open-source de engenheiros de software de IA autônomos, contando com mais de **70.000 stars no GitHub**, ecossistema corporativo com o **Agent Control Plane**, suporte a Kubernetes/KVM e oferta gerenciada OpenHands Cloud.

## Visão Geral
O **OpenHands** (mantido pela **All-Hands-AI**) é uma plataforma aberta para a criação e execução de agentes autônomos de engenharia de software. Capaz de atuar como um desenvolvedor parceiro ou individual, o agente navega autonomamente por repositórios, elabora planos formais, escreve código, executa compilações e testes em terminais isolados e resolve falhas de ponta a ponta.

## Principais Funcionalidades e Novidades (2025–2026)
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
- **Totalmente Agnóstico e Sem Lock-in:** Suporte irrestrito aos principais modelos do mercado (Claude Sonnet/Opus, GPT-4o/o3, Gemini, DeepSeek e modelos locais via Ollama/vLLM).
- **Transparência e Auditabilidade:** Código 100% open-source sob licença permissiva MIT.
- **Prontidão Enterprise:** Arquitetura desenhada para execução em nuvem e clusters corporativos.

### Limitações
- **Consumo de Hardware e Tokens:** Ambientes complexos com múltiplos ciclos de tentativa-e-erro em compilações pesadas demandam alto uso computacional e de tokens.
- **Configuração de Sandbox:** Setup inicial com Docker ou Kubernetes pode exigir esforço de infraestrutura em ambientes corporativos com restrições severas de rede.

## Casos de Uso
- Resolução autônoma de *issues* e bugs no GitHub/GitLab com submissão direta de Pull Requests prontos.
- Modernização, migração de frameworks e refatoração de bases de código legadas em grande escala.
- Prototipagem acelerada de microsserviços e aplicações web completas.
- Operações de engenharia gerenciadas em larga escala via Agent Control Plane.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT) e versão gerenciada (OpenHands Cloud).
- **Preço:** Gratuito em modo Self-Hosted (o usuário provê chaves de API ou modelos locais); planos sob demanda no OpenHands Cloud.
- **Agnóstico de Provedor:** Sim (100% agnóstico).

## Links Úteis
- **Site Oficial:** [https://www.all-hands.dev/](https://www.all-hands.dev/)
- **Repositório Oficial (GitHub):** [https://github.com/All-Hands-AI/OpenHands](https://github.com/All-Hands-AI/OpenHands)
- **OpenHands Cloud:** [https://openhands.dev/](https://openhands.dev/)
