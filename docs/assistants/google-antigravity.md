# Google Antigravity

> [!NOTE]
> O Google Antigravity representa a transição definitiva do modelo de "copiloto" (autocomplete síncrono) para o paradigma de **"agente autônomo"**, onde a IA atua como um parceiro de engenharia completo e independente.

## Visão Geral
O **Google Antigravity** é uma plataforma de desenvolvimento *agent-first* avançada desenvolvida pela equipe do **Google DeepMind**. Anunciada originalmente em novembro de 2025 juntamente com a família de modelos Gemini 3, a plataforma foi criada para funcionar como uma "central de controle" (home base) do desenvolvedor no desenvolvimento de software assistido por agentes autônomos. 

Com o lançamento recente do **Antigravity 2.0**, a plataforma evoluiu de uma extensão integrada de editor para uma **aplicação desktop standalone completa**, que serve como camada de orquestração superior do sistema operacional para automatizar fluxos complexos de engenharia.

---

## Interfaces e Versões da Plataforma
O ecossistema do Antigravity é distribuído em quatro formatos modulares e complementares:

*   **Ambiente Standalone (Antigravity 2.0):** Uma aplicação desktop completa e independente para macOS, Windows e Linux. Funciona como a central de controle de missões, desacoplando a execução dos agentes de um editor específico e permitindo a gestão global de repositórios e fluxos assíncronos.
*   **Editor View (IDE Integrada):** Um fork customizado do Visual Studio Code para interações síncronas de escrita de código. Fornece uma experiência premium de autocompletar multilinha, chat lateral de contexto e visualização de diffs interativos na tela.
*   **Antigravity CLI:** Uma interface de terminal leve e de alto desempenho projetada para fluxos de trabalho locais rápidos, scripts automatizados e fácil integração em pipelines de Integração Contínua (CI/CD).
*   **Antigravity SDK:** Um conjunto de ferramentas programáticas que permite a desenvolvedores e equipes de engenharia de software integrar a inteligência agentic do Antigravity diretamente em suas próprias aplicações e sistemas internos.

---

## Funcionalidades e Recursos Avançados

### 1. Orquestração e Paralelização de Tarefas
*   **Subagentes Dinâmicos:** Diante de tarefas complexas e extensas, o agente principal do Antigravity pode instanciar e gerenciar subagentes especializados de forma autônoma, paralelizando a execução de tarefas (ex: enquanto um subagente refatora o back-end, outro ajusta a folha de estilos do front-end).
*   **Execução Assíncrona no Background:** Processamento assíncrono de fluxos longos (builds, execuções de suites de testes complexos, etc.), liberando o desenvolvedor para continuar outras tarefas locais.
*   **Agendamento de Rotinas (Scheduled Tasks):** Um planejador de tarefas integrado que permite configurar execuções recorrentes ou temporizadores únicos através do comando `/schedule` ou interface gráfica, automatizando checagens de integridade ou análises de dependências periódicas.

### 2. Acesso à Área de Trabalho e Ambiente Seguro
*   **Navegador Integrado (Browser Subagent):** Capacidade autônoma de abrir, ler e interagir com navegadores web reais para coletar documentações atualizadas em tempo real, pesquisar APIs e realizar auditorias de layout ou fluxos end-to-end.
*   **Integração de Plugins & Skills:** Extensibilidade aprimorada através de plugins como o **Chrome DevTools**, permitindo que o agente inspecione o console de erros, analise requisições de rede ou interaja com o DOM para validar interfaces web desenvolvidas.
*   **Projetos Multi-Pasta (Multi-folder):** Flexibilidade para gerenciar bases de código espalhadas por diferentes diretórios e repositórios dentro de um mesmo escopo de "Projeto", superando as restrições tradicionais de limite de pastas.

### 3. Redução da Lacuna de Confiança (Trust Gap)
*   **Sistema de Artefatos Verificáveis:** Em vez de logs brutos e difíceis de interpretar, o Antigravity gera documentos estruturados de entrega como planos de implementação, listas de tarefas dinâmicas, relatórios de alteração, gravações do navegador e capturas de tela das validações visuais.
*   **Guardrails e JSON Hooks:** Configurações flexíveis por meio de arquivos JSON para estabelecer restrições de diretórios, níveis de permissões de leitura/escrita e interceptar ações sensíveis de execução de comandos no terminal.

---

## Pontos Fortes e Diferenciais
*   **Transparência nas Ações:** O acompanhamento passo a passo por meio de artefatos visuais confere alta previsibilidade ao trabalho do agente.
*   **Suporte Multi-Modelo Abrangente:** Embora otimizado e integrado nativamente à inteligência de raciocínio da família Gemini da Google (como o **Gemini 3.5 Flash** e **Gemini 3.1 Pro**), ele suporta nativamente o uso integrado de modelos de terceiros de alta capacidade como Anthropic Claude (Sonnet/Opus) e variantes do OpenAI GPT.
*   **Modo de Raciocínio (Planning Mode):** Metodologia nativa que força a IA a mapear arquiteturas e detalhar o plano de ação antes de realizar qualquer alteração nos arquivos de código.

---

## Casos de Uso Comuns
*   **Desenvolvimento E2E (Front-end ao Back-end):** Implementação completa de novas funcionalidades funcionais integradas.
*   **Depuração Avançada:** Execução assíncrona de suites de testes locais com detecção de falhas e aplicação de correções automáticas de dependências.
*   **Manutenção de Código Legado:** Refatorações pesadas com garantia de cobertura e validação por meio do browser agent integrado.

---

## Acesso e Preços
*   **Camada Individual:** Disponível em preview público com cota de uso gratuita robusta para fins de avaliação e desenvolvimento pessoal.
*   **Camada Enterprise:** Integração segura de nível corporativo e governança de dados simplificada por meio do *Gemini Enterprise Agent Platform*.

---

## Links Úteis
*   **Site Oficial do Antigravity:** [https://antigravity.google](https://antigravity.google)
*   **Google DeepMind:** [https://deepmind.google](https://deepmind.google)
