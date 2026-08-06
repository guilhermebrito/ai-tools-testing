# Paperclip

## Visão Geral
O Paperclip é uma plataforma open-source dedicada a fornecer a orquestração via *dashboard* UI-driven de sistemas multi-agentes de Inteligência Artificial. Diferente dos agentes focados estritamente na escrita de código, o Paperclip desempenha o papel de "Empresa" ou gerenciador de contexto em que os trabalhadores operam.

## Principais Funcionalidades / Como Funciona
- **Arquitetura BYOA (Bring-Your-Own-Agent):** É projetado para ser agnóstico sobre os "trabalhadores". O desenvolvedor pode injetar agentes construídos em Bash, Python puro, ou *wrappers* de outras LLMs no ecossistema Paperclip.
- **Heartbeats & Filas Resilientes:** Monitora ativamente os agentes com *heartbeats* e gerencia filas de tarefas demoradas, permitindo execuções assíncronas duradouras (7 dias de refatoração, por exemplo).
- **Controle de Orçamento:** Integra mecanismos rigorosos de limites (*hard caps*) financeiros baseados em tokens para evitar gastos exponenciais se um LLM ficar preso em loop.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Resolução da "Amnésia" de IAs (Statelessness):** A persistência forçada no banco de dados assegura que, em caso de instabilidade da rede ou da máquina virtual, todo o histórico e contexto não é perdido.
- **Orquestração Visual Intuitiva:** O painel UI centraliza a observabilidade das conversas e estados dos agentes (estilo Kanban).

### Limitações
- Trata-se de uma ferramenta orquestradora (uma "casca"); a eficiência total repousa nas ferramentas e LLMs que você plugar nele.
- Overheads operacionais de *setup* de banco de dados (geralmente Postgres/Redis).

## Casos de Uso
- Operações DevOps onde um *pipeline* complexo exija que múltiplos agentes (Analista, Desenvolvedor, DBA, QA) atuem sequencialmente.
- Projetos monumentais de modernização de legado.
- Prevenção rigorosa e monitoramento contra consumo exacerbado de orçamento computacional nas LLMs comerciais.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source.
- **Preço:** Totalmente gratuito, com a opção de hospedagem na máquina local (*Self-Hosted*).
- **Agnóstico de Provedor:** Sim.

## Links Úteis
- **Site Oficial:** [https://paperclip.dev/](https://paperclip.dev/)
- **Repositório Oficial (GitHub):** [https://github.com/paperclip-dev/paperclip](https://github.com/paperclip-dev/paperclip)
