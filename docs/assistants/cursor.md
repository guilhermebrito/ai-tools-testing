# Cursor

> [!NOTE]
> Com o lançamento do **Cursor v4.0** (agosto/setembro de 2026), a ferramenta consolida-se como uma **plataforma completa de agentes e engenharia autônoma**, introduzindo o **Max Mode** para raciocínio profundo com contexto massivo, o sistema de **Memories** persistentes, suporte expandido ao **Model Context Protocol (MCP)** e integrações nativas com **Linear** e **Notion** ao lado do Jira, além do novo plano **Ultra**.

## Visão Geral
O **Cursor** é a IDE AI-first pioneira e mais amplamente adotada no mercado, construída sobre um *fork* do VS Code com compatibilidade completa ao ecossistema de extensões. Com a chegada do **Cursor v4.0** (lançado entre agosto e setembro de 2026), o Cursor expandiu sua arquitetura para orquestração agentic de ponta a ponta, oferecendo suporte nativo aos modelos de linguagem mais avançados da indústria — como o **Claude 4.5 Sonnet** e as mais recentes variantes da família **GPT** da OpenAI —, permitindo tanto assistência de código síncrona quanto a execução de agentes autônomos em background na nuvem.

## Principais Funcionalidades e Novidades (2025–2026)
- **Assistência e Edição Síncrona:**
  - **Cursor Tab:** Previsão multi-linha e multi-arquivo em tempo real (*ghost text*), antecipando intenções e refatorações em cadeia.
  - **Composer (Cmd+I / Ctrl+I):** Motor aprimorado para geração e edição concorrente de múltiplos arquivos com renderização de *diffs* visuais inline e aceitação seletiva.
  - **Max Mode:** Novo modo de operação introduzido no Cursor v4.0 com janela de contexto expandida e raciocínio aprofundado (*deep reasoning*), evitando podas agressivas de contexto para resolver problemas arquiteturais e analisar bases de código volumosas.
  - **Memories (Memória Persistente):** Sistema de memória contínua entre sessões que retém preferências de codificação, convenções do repositório e decisões de design do desenvolvedor ao longo do tempo.
  - **Contexto Avançado (@) e Suporte Expandido a MCP:** Menções dinâmicas a repositórios completos, pastas, símbolos lógicos, git commits e documentações web, integrado de forma nativa e abrangente ao **Model Context Protocol (MCP)** para conexão com ferramentas externas, servidores locais e bancos de dados.
  - **Modelos de Ponta Atualizados:** Suporte integrado aos modelos mais recentes, incluindo **Claude 4.5 Sonnet** e as novas variantes do **GPT**.
- **Orquestração de Agentes Assíncronos:**
  - **Background Agents Aprimorados:** Suporte a tarefas assíncronas mais longas e complexas na nuvem (refatorações pesadas, criação de suítes de teste e implementação de features), trazendo mecanismos avançados de recuperação de falhas (*failure recovery*) e auto-correção durante a geração de PRs e branches.
  - **Agents Window:** Central de comando integrada na IDE para monitorar, pausar e orquestrar múltiplos agentes rodando em paralelo.
  - **BugBot Expandido:** Revisor de código autônomo acoplado ao GitHub que analisa Pull Requests e agora detecta proativamente **vulnerabilidades de segurança** e **problemas de performance/desempenho** além de bugs lógicos, fornecendo links diretos "Fix in Cursor" e configuração customizada via `.cursor/BUGBOT.md`.
  - **Automations (Multi-Repo & No-Repo):** Rotinas agentic capazes de operar através de múltiplos repositórios ou executar tarefas sem repo associado (ex: monitorar canais de Slack, métricas de observabilidade ou tickets de backlog).
  - **Ecossistema de Integrações de Tarefas (Jira, Linear e Notion):** Conexão bidirecional que permite atribuir issues e especificações não apenas do Jira, mas também do **Linear** e do **Notion** diretamente para agentes do Cursor realizarem diagnósticos, planejamento e implementações automáticas.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Experiência do Desenvolvedor (UX):** Transição suave para usuários do VS Code com sensação de fluidez e velocidade na digitação assistida.
- **Paralelismo com Background Agents Resilientes:** Desacopla tarefas demoradas da máquina local com maior tolerância a falhas, aumentando exponencialmente o throughput de engenharia.
- **Raciocínio Profundo com Max Mode:** Análise arquitetural aprofundada em projetos de grande escala sem perda de contexto relevante.
- **Personalização Contínua com Memories:** Aprendizado orgânico do estilo do desenvolvedor e convenções de projeto sem necessidade de instruções repetitivas.
- **Qualidade de Revisão com BugBot:** Inspeção automatizada em nível de PR reduzindo regressões, vulnerabilidades de segurança e gargalos de performance antes do merge.
- **Extensibilidade via MCP:** Interoperabilidade padronizada com ferramentas corporativas, APIs e fontes de dados externas.

### Limitações
- **Fork Proprietário:** Fica sujeito ao ciclo de sincronização de patches upstream da base do VS Code.
- **Consumo de Memória:** Indexação semântica profunda de grandes monorepos pode demandar alto consumo de hardware local.

## Casos de Uso
- Pair programming contínuo no dia a dia com Cursor Tab e Composer.
- Resolução de problemas arquiteturais complexos e refatorações estruturais usando o **Max Mode**.
- Delegação assíncrona de refatorações complexas e escrita de testes para Background Agents com recuperação de falhas.
- Triagem automática, auditoria de segurança e análise de performance em Pull Requests com BugBot.
- Automação e implementação de tarefas a partir de tickets e especificações no **Jira**, **Linear** e **Notion**.
- Integração de contexto corporativo, bancos de dados e ferramentas customizadas via **MCP**.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário (baseado no VS Code).
- **Preço:**
  - **Plano Hobby (Gratuito):** Acesso inicial básico para completions e limites de chat.
  - **Plano Pro ($20/mês):** Acesso completo e prioritário ao Cursor Tab, Composer e modelos de fronteira.
  - **Plano Business ($40/mês por usuário):** Inclui Background Agents, BugBot, Automations multi-repo e recursos de governança de equipe.
  - **Plano Ultra ($200/mês) (Novo):** Tier premium voltado a usuários intensivos (*power users*), oferecendo limites amplamente expandidos (cerca de 20x mais uso em relação ao Pro), créditos substanciais para modelos de ponta, maior concorrência para Background Agents e acesso prioritário ao Max Mode.
- **Agnóstico de Provedor:** Suporta nativamente modelos de ponta da Anthropic (incluindo Claude 4.5 Sonnet), OpenAI (últimas variantes GPT) e Google, além de servidores MCP e chaves de API customizadas.

## Links Úteis
- **Site Oficial:** [https://cursor.com/](https://cursor.com/)
- **Documentação:** [https://docs.cursor.com/](https://docs.cursor.com/)
- **Changelog Oficial:** [https://cursor.com/changelog](https://cursor.com/changelog)
- **Model Context Protocol (MCP):** [https://modelcontextprotocol.io/](https://modelcontextprotocol.io/)
