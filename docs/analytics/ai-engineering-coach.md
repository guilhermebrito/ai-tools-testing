# AI Engineer Coach (Microsoft)

> [!NOTE]
> O AI Engineer Coach é uma ferramenta de **observabilidade local e engenharia reversa de hábitos**, desenvolvida pela Microsoft para transformar logs brutos de assistentes de IA em diagnósticos acionáveis, métricas de produtividade e detecção de anti-padrões com privacidade estrita (100% offline). Com as atualizações recentes de outubro de 2026, a ferramenta expandiu sua cobertura para **mais de 55 anti-padrões**, refinou a compatibilidade com logs de **Claude Code**, **Cursor** e **Google Antigravity** (além do GitHub Copilot), trouxe visualizações detalhadas de tendências temporais e introduziu o **Team Mode (Preview)** para lideranças técnicas.

## Visão Geral
O **AI Engineer Coach** é uma extensão open-source para Visual Studio Code (v1.115+) criada pela equipe de engenharia da **Microsoft**. Ela atua como um treinador analítico contínuo para desenvolvedores que utilizam assistentes de código e agentes de IA — incluindo GitHub Copilot, Claude Code, Cursor e Google Antigravity, abrangendo interações com os modelos de ponta mais recentes, como Claude 3.7 Sonnet, Claude Sonnet 4, Gemini 2.5 Pro, Gemini 2.5 Flash e GPT-4o —, interpretando os logs locais das sessões de trabalho para apontar melhorias de engenharia de prompt, higiene de contexto e qualidade de revisão.

## Principais Funcionalidades e Novidades (2025–2026)
- **Detecção Contínua de Anti-Padrões (+55 Regras):**
  - Mapeia mais de 55 vícios e erros metodológicos em cinco pilares fundamentais: qualidade de prompt, higiene de sessão (sessões longas demais ou sem foco), rigor de revisão humana de código, domínio de ferramentas (tool calling) e gestão de contexto.
- **Compatibilidade Aprimorada Multi-Assistente:**
  - Ingestão e normalização refinada de logs locais de múltiplos ecossistemas, oferecendo suporte robusto para **Claude Code**, **Cursor** e **Google Antigravity**, além do **GitHub Copilot**, permitindo consolidar diagnósticos mesmo para quem alterna ferramentas e CLIs no fluxo de trabalho.
- **Painel Analítico Aprimorado e Visualização de Tendências:**
  - Visualizações detalhadas e aprofundadas de tendências de produtividade ao longo do tempo, facilitando o acompanhamento histórico da evolução metodológica e da eficiência no uso de agentes de IA.
  - Métricas práticas de score de adoção, mapas de calor diários e gráficos de evolução temporal de volume de código gerado vs. código modificado manualmente.
  - Segmentação detalhada por linguagem de programação, workspace, modelo de IA e plataforma/harness utilizado.
- **Team Mode (Preview Experimental):**
  - Funcionalidade experimental projetada para tech leads e lideranças técnicas visualizarem métricas agregadas de produtividade e padrões de adoção em nível de time.
  - Arquitetura estritamente orientada à privacidade com consentimento explícito (*privacy opt-in*) e consolidação anônima de dados, preservando a confidencialidade do código e das sessões individuais.
- **Skill Discovery (Descoberta Automática de Skills):**
  - Algoritmo de clustering que identifica padrões repetitivos de instruções e prompts no histórico e sugere sua automação como "skills" ou templates reutilizáveis.
- **Auditoria de Prontidão de Contexto (Context Health):**
  - Varredura de integridade de arquivos de instrução de agentes (`.cursorrules`, `CLAUDE.md`, `.gemini/rules`), alertando sobre regras conflitantes, instruções prolixas e mapas de contexto desatualizados.
- **Privacidade Local Absoluta (Offline First):**
  - Todo o processamento estatístico e parsing de logs ocorre exclusivamente na máquina do desenvolvedor; nenhum dado de telemetria, código-fonte ou transcrição de chat é enviado para servidores externos.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Privacidade Total:** Inviolabilidade de código e conformidade de dados para ambientes corporativos ultrarestritos, estendida ao Team Mode via opt-in estrito.
- **Transparência e Melhoria Contínua:** Permite que desenvolvedores meçam empiricamente seu ganho de produtividade com IA e visualizem tendências ao longo do tempo, em vez de depender de percepções subjetivas.
- **Independência de Provedor e Ampla Compatibilidade:** Analisa e normaliza logs de múltiplos assistentes (Copilot, Claude Code, Cursor, Antigravity) sem fidelidade forçada a um único ecossistema.
- **Visibilidade de Equipe com Governança:** O Team Mode (Preview) oferece aos líderes técnicos percepções acionáveis sobre a maturidade da equipe sem violar a privacidade dos desenvolvedores.

### Limitações
- **Restrito ao VS Code:** Atualmente disponível exclusivamente como extensão da interface VS Code (v1.115+).
- **Dependência de Formato de Logs:** A precisão das análises depende da persistência e consistência dos logs gerados pelos assistentes instalados.
- **Fase Experimental do Team Mode:** O modo em equipe está em estágio de Preview, exigindo configuração de opt-in pelos participantes.

## Casos de Uso
- Auditoria pessoal para identificar dependência cega (*blind acceptance*) de código de IA e reforçar a revisão humana com base em mais de 55 anti-padrões catalogados.
- Acompanhamento de tendências temporais de produtividade para quantificar a curva de aprendizado no uso de ferramentas agentic.
- Diagnóstico unificado de sessões em fluxos híbridos que combinam diferentes assistentes (Copilot, Cursor, Claude Code, Antigravity).
- Visão agregada de maturidade agentic e suporte a decisões de mentoria para tech leads através do Team Mode.
- Diagnóstico de bloated context e otimização de arquivos de regras para agentes de IA.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT, mantido pela Microsoft).
- **Preço:** Totalmente gratuito (incluindo o Team Mode em preview).
- **Agnóstico de Provedor:** Sim (analisa múltiplos assistentes locais).

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/microsoft/AI-Engineering-Coach](https://github.com/microsoft/AI-Engineering-Coach)
