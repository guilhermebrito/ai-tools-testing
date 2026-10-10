# Traycer AI

> [!NOTE]
> Com o lançamento do **Traycer 2.0** (outubro de 2026), a plataforma consolida-se como a **camada de governança e orquestração spec-first**: em vez de substituir seus agentes favoritos (Cursor, Claude Code, Windsurf), ele atua a montante definindo especificações visuais e formais, gerenciando o handoff multi-agente e verificando a integridade das alterações antes da fusão em Pull Requests.

## Visão Geral
O **Traycer AI** é uma plataforma desenhada para transformar a engenharia de software assistida por IA através da abordagem **spec-first** (especificação em primeiro lugar). Com a chegada do **Traycer 2.0** em outubro de 2026 — uma grande atualização da plataforma —, o sistema amplia a governança arquitetural sobre os mais recentes modelos de fronteira e raciocínio (como Claude 3.7 Sonnet, GPT-4o, OpenAI o3-mini e Gemini 2.0/2.5), coordenados diretamente em ferramentas líderes como Cursor, Claude Code e Windsurf. Posicionando-se entre os times humanos e os agentes autônomos de código, o Traycer substitui o improviso do *vibe coding* por contratos arquiteturais explícitos, garantindo rastreabilidade contínua, decomposição visual e consistência mesmo em bases de código legadas e de alta complexidade.

## Principais Funcionalidades e Novidades (2025–2026)
- **Engenharia Spec-First contra Vibe Coding:**
  - Exige a definição formal de objetivos, restrições e casos de borda antes de qualquer modificação de código, sintetizando especificações acionáveis que servem de guia rígido para os agentes.
- **Traycer 2.0 e Visual Spec Editor (Editor Visual de Specs):**
  - Nova interface visual intuitiva para criação, modelagem e edição de especificações técnicas, tornando a metodologia spec-first acessível não apenas a desenvolvedores experientes, mas também a gerentes de produto, designers e stakeholders não técnicos.
- **Integração Nativa com GitHub (PRs e Issues):**
  - Vinculação direta e bidirecional de especificações a Pull Requests e Issues do GitHub, automatizando a rastreabilidade do ciclo de vida das tarefas e viabilizando a validação de conformidade no fluxo Git diário da equipe.
- **Orquestração Multi-Agente Aprimorada e Parcerias Oficiais:**
  - Suporte otimizado para orquestrar múltiplos agentes de execução (**Cursor**, **Claude Code** e **Windsurf**) a partir de uma única especificação centralizada. O Traycer 2.0 oficializou parcerias e integrações nativas com o Cursor e o Claude Code para transferências de contexto otimizadas e handoff sem atritos.
- **Painel Centralizado de Verificação (Verification Dashboard):**
  - Visão consolidada em tempo real para monitorar o status de validação de todas as especificações ativas no workspace, alertando sobre discrepâncias de escopo, falhas em testes e regressões antes do merge.
- **Decomposição em Fases e Milestones:**
  - Quebra requisitos de alto nível em etapas sequenciais com dependências claras, permitindo revisão granular e intervenções humanas sem reiniciar todo o contexto.
- **Handoff Inteligente para Agentes de Execução:**
  - Delega a execução prática das fases para os agentes de codificação preferidos pelo time (**Cursor**, **Claude Code**, **Windsurf**, **Google Antigravity**), injetando apenas o subconjunto de contexto relevante para cada micro-tarefa.
- **Motor de Verificação Automática (Closed-Loop Verification):**
  - Analisa as modificações de código submetidas pelos agentes contra as especificações originais e suítes de teste, detectando alucinações, vazamentos de escopo ou regressões antes da abertura e aprovação de Pull Requests.
- **Preservação e Durabilidade da Intenção:**
  - Mantém a árvore de decisões arquiteturais e o raciocínio por trás de cada mudança persistidos no repositório, garantindo que sessões futuras de IA ou novos engenheiros compreendam o histórico do projeto.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Aderência Arquitetural Rigorosa:** Garante que agentes executem exatamente o que foi planejado, prevenindo mutações descontroladas no design do software.
- **Compatibilidade Aditiva e Parcerias Oficiais:** Não exige abandono das ferramentas que os desenvolvedores já dominam; potencializa Cursor e Claude Code por meio de integrações diretas e governança upstream.
- **Acessibilidade para Não Desenvolvedores:** O Visual Spec Editor democratiza a criação e revisão de especificações para times multidisciplinares.
- **Rastreabilidade Nativa via GitHub:** Vinculação de specs a PRs e Issues fecha o ciclo de auditoria e conformidade corporativa.
- **Redução Drástica de Retrabalho:** A verificação automática combinada ao Verification Dashboard barra alterações defeituosas no início do ciclo de revisão.

### Limitações
- **Cultura e Disciplina:** Demanda mudança cultural de desenvolvedores habituados a pedir código imediato sem planejamento formal.
- **Etapa Adicional no Ciclo:** Pode adicionar fricção temporária para scripts pontuais ou alterações cosméticas triviais.

## Casos de Uso
- Arquiteturas corporativas complexas com requisitos severos de auditoria, conformidade e manutenibilidade.
- Orquestração coordenada de múltiplos desenvolvedores e agentes trabalhando em módulos interdependentes a partir de uma única spec.
- Grandes migrações de stack e refatorações de sistemas críticos de negócio.
- Colaboração cross-funcional entre gerentes de produto, designers e engenheiros antes do início da codificação por agentes.

## Status, Preço e Licenciamento
- **Modelo:** Plataforma comercial / Camada de Orquestração Spec-First.
- **Preço:** Plano gratuito expandido (com maior cota mensal de especificações e verificações para desenvolvedores individuais) e tiers pagos (Team/Enterprise) para times e empresas com suporte a workspaces colaborativos e governança avançada.
- **Agnóstico de Provedor/Agente:** Sim (100% agnóstico de ferramentas de código e provedores de LLM, com integrações oficiais otimizadas para Cursor, Claude Code e Windsurf).

## Links Úteis
- **Site Oficial:** [https://traycer.ai/](https://traycer.ai/)
- **Documentação Oficial:** [https://docs.traycer.ai/](https://docs.traycer.ai/)
- **Repositório GitHub:** [https://github.com/traycerai/traycer](https://github.com/traycerai/traycer)
