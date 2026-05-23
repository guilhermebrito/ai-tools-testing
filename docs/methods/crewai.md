# CrewAI

## Visão Geral
CrewAI é um framework poderoso em Python construído para estruturar, orquestrar e gerenciar "times" (crews) de agentes de IA autônomos. Ele permite que desenvolvedores definam diferentes agentes com papéis específicos, metas e ferramentas, fazendo-os trabalhar em conjunto de forma colaborativa para completar tarefas complexas.

## Funcionalidades Principais
- **Design Baseado em Papéis (Role-based):** Permite a definição de agentes focados em papéis específicos (ex: 'Engenheiro Sênior', 'Especialista de QA', 'Product Manager'), atribuindo a cada um um *backstory* e uma meta focada.
- **Delegação e Colaboração:** Agentes podem delegar subtarefas uns aos outros, discutir e compartilhar contexto em tempo real, viabilizando a resolução de problemas em múltiplas etapas lógicas.
- **Integração de Ferramentas:** Possui integração nativa com o ecossistema LangChain, permitindo que os agentes utilizem diversas ferramentas como busca na web, execução de código, leitura de arquivos locais, acesso a banco de dados, etc.
- **Agnosticismo de Modelos:** Flexibilidade total em relação aos LLMs utilizados. Você pode ter um time onde o 'Desenvolvedor' usa Claude 3.5 Sonnet, o 'Revisor' usa GPT-4o e o 'Pesquisador' usa um modelo Llama local.

## Casos de Uso
- Geração de código estruturado onde um agente escreve o código, outro agente revisa contra boas práticas e um terceiro agente cria os testes.
- Automação de processos complexos que requerem múltiplas etapas de revisão e tomada de decisão lógica.
- Criação de pipelines complexos de dados (pesquisa na web, sumarização e formatação).

## Status
- **Open Source:** Sim (Licença MIT).
- **Agnóstico de Modelo:** Sim.

## Links Úteis
- **Site Oficial / Documentação:** [https://www.crewai.com/](https://www.crewai.com/)
- **Repositório Oficial (GitHub):** [https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)
