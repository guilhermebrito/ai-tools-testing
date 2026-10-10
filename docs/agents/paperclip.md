# Paperclip

> [!NOTE]
> O Paperclip não é um agente isolado — é o **sistema operacional e controle de missão** para frotas multi-agente, organizando múltiplos agentes autônomos em uma estrutura empresarial (Org-Chart) com governança, templates pré-configurados e persistência duradoura.

## Visão Geral
O **Paperclip** é uma plataforma open-source de orquestração empresarial orientada por interface gráfica (UI-driven) lançada em 2026. Operando sob a filosofia **"Bring Your Own Agent" (BYOA)**, ela permite conectar agentes heterogêneos baseados nos modelos mais recentes do mercado (como Claude 3.7 Sonnet, Claude 3.5 Sonnet, GPT-4o, o1, o3-mini, Gemini 2.5 e DeepSeek-R1) e runtimes como Claude Code, Codex, Hermes, OpenHands ou scripts customizados em Python/Bash. A plataforma estrutura esses agentes como um time colaborativo com hierarquias bem definidas, filas de tarefas assíncronas e supervisão centralizada.

## Principais Funcionalidades e Novidades (2025–2026)
- **Estrutura Organizacional e Org-Chart Visual:**
  - Mapeamento hierárquico de agentes com definição de cargos (CEO, Tech Lead, Engenheiro de Software, QA, DevOps), descrições de função (*job descriptions*) e linhas diretas de reporte e delegação.
  - **Templates de Organograma (Org-Chart Templates):** Modelos pré-configurados de estruturas organizacionais para agentes, simplificando e agilizando o setup inicial de equipes e fluxos de trabalho.
- **Heartbeat System e Filas Resilientes:**
  - Sistema de sinais vitais periódicos em que agentes "acordam", consultam suas filas assíncronas de trabalho, executam tarefas e registram o status. Evita conexões presas em loop e mantém tarefas ativas por dias de forma resiliente.
- **Governança Orçamentária e Perfis de Custo:**
  - Limites rígidos de gastos (*budget hard caps*) por agente com pausa automática ao atingir a cota.
  - Seleção dinâmica de perfis de modelos mais baratos (*cheaper model profiles*) para recuperação de falhas e tarefas triviais, otimizando o consumo de tokens.
- **Workflows de Aprovação (Human-in-the-Loop):**
  - Portais de aprovação humana para ações de alto impacto (ex: merges em branches principais, deploys de produção, compras ou chamadas financeiras).
- **Aprimoramentos no Servidor MCP (Model Context Protocol):**
  - Servidor nativo **MCP** integrado para facilitar o compartilhamento de contexto, ferramentas e fontes de dados entre agentes.
  - **Comunicação Cross-Agent Refinada:** Otimizações recentes no servidor MCP que aperfeiçoam a troca de contexto e a colaboração direta e coordenada entre múltiplos agentes heterogêneos.
- **Evolução do Dashboard em React:**
  - **Visualização Aprimorada de Custos:** Painéis aprimorados para rastreamento detalhado de gastos acumulados e consumo de tokens por agente e tarefa.
  - **Acompanhamento de Progresso dos Agentes:** Monitoramento granular do ciclo de vida, status e tarefas de cada agente em tempo real.
- **Integrações e Adaptadores Expandidos:**
  - Novos adaptadores modulares para conexão e orquestração de um catálogo ampliado de agentes autônomos, runtimes e ferramentas externas.
- **Persistência Contra Statelessness:**
  - Armazenamento centralizado em banco de dados que mantém todo o histórico de decisões e contexto intactos, garantindo continuidade mesmo após reinicializações de servidores ou contêineres.
- **Comunidade e Ecossistema em Expansão:**
  - Base crescente de contribuidores ativos no projeto open-source, acelerando a implementação de novos recursos, integrações e correções.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Agnosticismo Radical:** Funciona com qualquer modelo, qualquer runtime de agente e qualquer provedor de infraestrutura.
- **Observabilidade em Nível Executivo:** Dashboard React tipo "CEO view" que consolida progresso dos agentes em tempo real, visualização detalhada de custos e bloqueios operacionais.
- **Setup Acelerado:** Templates de organograma pré-construídos que diminuem sensivelmente o tempo de implementação de novas equipes de agentes.
- **Controle de Risco:** Previne estouros de orçamento e ações destrutivas através de auditoria e aprovações obrigatórias.

### Limitações
- **Requer Infraestrutura Própria:** A instalação self-hosted depende de setup de serviços como PostgreSQL, Redis e contêineres Docker.
- **Não Gera Código Diretamente:** A performance técnica final depende da qualidade dos agentes e LLMs conectados à plataforma.

## Casos de Uso
- Operação de times autônomos de desenvolvimento e QA executando refatorações multi-semanais.
- Pipelines de suporte técnico onde agentes de triagem delegam chamados a agentes de engenharia.
- Gestão centralizada de custos e governança de IA para empresas com dezenas de agentes ativos.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Self-Hosted).
- **Preço:** Gratuito (código aberto). Custos de infraestrutura e tokens de LLM sob responsabilidade do usuário.
- **Agnóstico de Provedor:** Sim (100% agnóstico).

## Links Úteis
- **Site Oficial:** [https://paperclip.ing/](https://paperclip.ing/)
- **Repositório Oficial (GitHub):** [https://github.com/paperclip-dev/paperclip](https://github.com/paperclip-dev/paperclip)
