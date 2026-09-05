# AI Engineer Coach (Microsoft)

> [!NOTE]
> O AI Engineer Coach é uma ferramenta de **observabilidade local e engenharia reversa de hábitos**, desenvolvida pela Microsoft para transformar logs brutos de assistentes de IA em diagnósticos acionáveis, métricas de produtividade e detecção de anti-padrões com privacidade estrita (100% offline).

## Visão Geral
O **AI Engineer Coach** é uma extensão open-source para Visual Studio Code (v1.115+) criada pela equipe de engenharia da **Microsoft**. Ela atua como um treinador analítico contínuo para desenvolvedores que utilizam assistentes de código e agentes de IA (como GitHub Copilot, Claude Code, Cursor, entre outros), interpretando os logs locais das sessões de trabalho para apontar melhorias de engenharia de prompt, higiene de contexto e qualidade de revisão.

## Principais Funcionalidades e Novidades (2025–2026)
- **Detecção Contínua de Anti-Padrões (+45 Regras):**
  - Mapeia vícios e erros metodológicos em cinco pilares fundamentais: qualidade de prompt, higiene de sessão (sessões longas demais ou sem foco), rigor de revisão humana de código, domínio de ferramentas (tool calling) e gestão de contexto.
- **Painel Analítico de Produtividade e Métricas Agentic:**
  - Métricas práticas de score de adoção, mapas de calor diários e gráficos de evolução semanal de volume de código gerado vs. código modificado manualmente.
  - Segmentação detalhada por linguagem de programação, workspace, modelo de IA e plataforma/harness utilizado.
- **Skill Discovery (Descoberta Automática de Skills):**
  - Algoritmo de clustering que identifica padrões repetitivos de instruções e prompts no histórico e sugere sua automação como "skills" ou templates reutilizáveis.
- **Auditoria de Prontidão de Contexto (Context Health):**
  - Varredura de integridade de arquivos de instrução de agentes (`.cursorrules`, `CLAUDE.md`, `.gemini/rules`), alertando sobre regras conflitantes, instruções prolixas e mapas de contexto desatualizados.
- **Privacidade Local Absoluta (Offline First):**
  - Todo o processamento estatístico e parsing de logs ocorre exclusivamente na máquina do desenvolvedor; nenhum dado de telemetria, código-fonte ou transcrição de chat é enviado para servidores externos.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Privacidade Total:** Inviolabilidade de código e conformidade de dados para ambientes corporativos ultrarestritos.
- **Transparência e Melhoria Contínua:** Permite que desenvolvedores meçam empiricamente seu ganho de produtividade com IA, em vez de depender de percepções subjetivas.
- **Independência de Provedor:** Analisa múltiplos assistentes sem fidelidade forçada a um único ecossistema.

### Limitações
- **Restrito ao VS Code:** Atualmente disponível exclusivamente como extensão da interface VS Code (v1.115+).
- **Dependência de Formato de Logs:** A precisão das análises depende da persistência e consistência dos logs gerados pelos assistentes instalados.

## Casos de Uso
- Auditoria pessoal para identificar dependência cega (*blind acceptance*) de código de IA e reforçar a revisão humana.
- Padronização de boas práticas e métricas de maturidade agentic em equipes de engenharia de software.
- Diagnóstico de bloated context e otimização de arquivos de regras para agentes de IA.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT, mantido pela Microsoft).
- **Preço:** Totalmente gratuito.
- **Agnóstico de Provedor:** Sim (analisa múltiplos assistentes locais).

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/microsoft/AI-Engineering-Coach](https://github.com/microsoft/AI-Engineering-Coach)
