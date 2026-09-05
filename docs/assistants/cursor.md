# Cursor

> [!NOTE]
> O Cursor evoluiu de uma IDE com autocompletar inteligente para uma **plataforma completa de agentes assíncronos**, incorporando Background Agents na nuvem, o revisor autônomo BugBot, Automations multi-repo e integração bidirecional com Jira.

## Visão Geral
O **Cursor** é a IDE AI-first pioneira e mais amplamente adotada no mercado, construída sobre um *fork* do VS Code com compatibilidade completa ao ecossistema de extensões. Com a evolução para a **versão 3.5+**, o Cursor transformou-se em uma plataforma de orquestração agentic em que agentes trabalham paralelamente em background na nuvem enquanto o desenvolvedor edita código localmente.

## Principais Funcionalidades e Novidades (2025–2026)
- **Assistência e Edição Síncrona:**
  - **Cursor Tab:** Previsão multi-linha e multi-arquivo em tempo real (*ghost text*), antecipando intenções e refatorações em cadeia.
  - **Composer 2.5 (Cmd+I / Ctrl+I):** Motor aprimorado para geração e edição concorrente de múltiplos arquivos com renderização de *diffs* visuais inline e aceitação seletiva.
  - **Contexto Avançado (@):** Menções dinâmicas a repositórios completos, pastas, símbolos lógicos, git commits e documentações web em tempo real.
- **Orquestração de Agentes Assíncronos:**
  - **Background Agents:** Permite delegar tarefas demoradas (refatorações pesadas, criação de suítes de teste, implementação de features) para agentes que executam de forma assíncrona na nuvem, entregando PRs prontos ou branches para revisão.
  - **Agents Window:** Central de comando integrada na IDE para monitorar, pausar e orquestrar múltiplos agentes rodando em paralelo.
  - **BugBot:** Revisor de código autônomo acoplado ao GitHub que analisa Pull Requests, detecta bugs lógicos ou vulnerabilidades de segurança e adiciona links diretos "Fix in Cursor" para correção imediata.
  - **Automations (Multi-Repo & No-Repo):** Rotinas agentic capazes de operar através de múltiplos repositórios ou executar tarefas sem repo associado (ex: monitorar canais de Slack, métricas de observabilidade ou tickets de backlog).
  - **Integração com Jira:** Conexão direta que permite atribuir issues e tickets do Jira para agentes do Cursor realizarem diagnósticos e implementações automáticas.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Experiência do Desenvolvedor (UX):** Transição suave para usuários do VS Code com sensação de fluidez e velocidade na digitação assistida.
- **Paralelismo com Background Agents:** Desacopla tarefas demoradas da máquina local, aumentando exponencialmente o throughput de engenharia.
- **Qualidade de Revisão com BugBot:** Inspeção automatizada em nível de PR reduz significativamente a entrada de regressões e falhas de segurança na main branch.

### Limitações
- **Fork Proprietário:** Fica sujeito ao ciclo de sincronização de patches upstream da base do VS Code.
- **Consumo de Memória:** Indexação semântica profunda de grandes monorepos pode demandar alto consumo de hardware local.

## Casos de Uso
- Pair programming contínuo no dia a dia com Cursor Tab e Composer.
- Delegação assíncrona de refatorações complexas e escrita de testes para Background Agents.
- Triagem automática e auditoria de Pull Requests no GitHub com BugBot.
- Automação de tickets do Jira e fluxos integrados com múltiplos repositórios.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário (baseado no VS Code).
- **Preço:**
  - **Plano Hobby (Gratuito):** Acesso inicial básico para completions e limites de chat.
  - **Plano Pro ($20/mês):** Acesso completo e prioritário ao Cursor Tab, Composer e modelos de fronteira.
  - **Plano Business ($40/mês):** Inclui Background Agents, BugBot, Automations multi-repo e recursos de governança de equipe.
- **Agnóstico de Provedor:** Suporta nativamente modelos de ponta da OpenAI, Anthropic e Google, além de chaves de API customizadas.

## Links Úteis
- **Site Oficial:** [https://cursor.com/](https://cursor.com/)
- **Documentação:** [https://docs.cursor.com/](https://docs.cursor.com/)
- **Changelog Oficial:** [https://cursor.com/changelog](https://cursor.com/changelog)
