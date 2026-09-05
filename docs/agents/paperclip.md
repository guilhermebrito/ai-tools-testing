# Paperclip

> [!NOTE]
> O Paperclip não é um agente isolado — é o **sistema operacional e controle de missão** para frotas multi-agente, organizando múltiplos agentes autônomos em uma estrutura empresarial (Org-Chart) com governança e persistência duradoura.

## Visão Geral
O **Paperclip** é uma plataforma open-source de orquestração empresarial orientada por interface gráfica (UI-driven) lançada em 2026. Operando sob a filosofia **"Bring Your Own Agent" (BYOA)**, ela permite conectar agentes heterogêneos (como Claude Code, Codex, Hermes, OpenHands ou scripts customizados em Python/Bash) e estruturá-los como um time colaborativo com hierarquias, filas de tarefas assíncronas e supervisão centralizada.

## Principais Funcionalidades e Novidades (2025–2026)
- **Estrutura Organizacional e Org-Chart Visual:**
  - Mapeamento hierárquico de agentes com definição de cargos (CEO, Tech Lead, Engenheiro de Software, QA, DevOps), descrições de função (*job descriptions*) e linhas diretas de reporte e delegação.
- **Heartbeat System e Filas Resilientes:**
  - Sistema de sinais vitais periódicos em que agentes "acordam", consultam suas filas assíncronas de trabalho, executam tarefas e registram o status. Evita conexões presas em loop e mantém tarefas ativas por dias de forma resiliente.
- **Governança Orçamentária e Perfis de Custo:**
  - Limites rígidos de gastos (*budget hard caps*) por agente com pausa automática ao atingir a cota.
  - Seleção dinâmica de perfis de modelos mais baratos (*cheaper model profiles*) para recuperação de falhas e tarefas triviais, otimizando o consumo de tokens.
- **Workflows de Aprovação (Human-in-the-Loop):**
  - Portais de aprovação humana para ações de alto impacto (ex: merges em branches principais, deploys de produção, compras ou chamadas financeiras).
- **Extensibilidade e Protocolo MCP:**
  - Servidor nativo **MCP (Model Context Protocol)** integrado, facilitando a troca de contexto, ferramentas e fontes de dados entre diferentes runtimes de agentes sem código intermediário complexo.
- **Persistência Contra Statelessness:**
  - Armazenamento centralizado em banco de dados que mantém todo o histórico de decisões e contexto intactos, garantindo continuidade mesmo após reinicializações de servidores ou contêineres.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Agnosticismo Radical:** Funciona com qualquer modelo, qualquer runtime de agente e qualquer provedor de infraestrutura.
- **Observabilidade em Nível Executivo:** Dashboard React tipo "CEO view" que consolida progresso, custos acumulados e bloqueios de toda a organização de IA.
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
