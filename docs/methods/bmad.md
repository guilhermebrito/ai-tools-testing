# BMAD (Breakthrough Method for Agile AI-Driven Development)

> [!NOTE]
> O BMAD não é um software — é uma **metodologia open-source** que combate o "vibe coding" tratando a IA como um **time virtual de especialistas** com papéis definidos, documentação como fonte da verdade e um ciclo de vida de 4 fases.

## Visão Geral
O **BMAD** é um framework metodológico open-source desenhado para trazer estrutura, disciplina e práticas de engenharia de software profissional ao desenvolvimento assistido por IA. Em vez de usar um LLM como chatbot generalista, o BMAD organiza a interação em um **time ágil virtual** de agentes especializados que seguem um fluxo de trabalho rigoroso e repetível.

---

## Como Funciona

### Workflow Baseado em Personas
Em vez de interagir com um assistente único, o BMAD define agentes especializados com responsabilidades claras:
*   **Analyst:** Captura ideias e restrições em um product brief conciso.
*   **Product Manager (PM):** Gera Product Requirements Documents (PRDs) detalhados.
*   **Architect:** Projeta a arquitetura do sistema, stack e padrões.
*   **Developer:** Implementa o código baseando-se estritamente nos documentos gerados.
*   **Scrum Master:** Gerencia o progresso e prioriza tarefas.
*   **QA:** Verifica e valida implementações contra os requisitos.

### Documentação como Fonte da Verdade (Spec-Driven)
O método exige a criação de artefatos em Markdown (PRD, Architecture Specs, User Stories) que servem como "single source of truth". Quando o "Desenvolvedor" (IA) vai codar, ele recebe o contexto estrito desses documentos, **prevenindo alucinações** e drift de contexto.

### Ciclo de Vida de 4 Fases
1.  **Analysis:** Captura de ideias e restrições.
2.  **Planning:** Geração de PRDs detalhados.
3.  **Solutioning:** Design de arquitetura, stack e padrões.
4.  **Implementation:** Decomposição em user stories atômicas para dev e verificação QA.

---

## Evoluções (2026 — v6.x)

### Arquitetura em Camadas
O ecossistema BMAD agora está estruturado em três camadas:
*   **BMad Core:** Motor universal do framework para coordenação de agentes.
*   **BMad Method:** Módulo de desenvolvimento ágil com o ciclo de 4 fases.
*   **BMad Builder (BMB):** Toolkit para que equipes projetem, compartilhem e customizem seus próprios agentes e workflows.

### Inteligência Adaptativa de Escala
Versões modernas do BMAD ajustam automaticamente o rigor do planejamento com base na complexidade do projeto:
*   **Quick Flow:** Para bug fixes e alterações menores.
*   **Standard Flow:** Para features de tamanho médio.
*   **Enterprise Flow:** Para sistemas de larga escala com requisitos de compliance.

### Compatibilidade Cross-Platform
A versão v6.x introduziu suporte para executar configurações de agentes de forma transparente em diversas IDEs e ferramentas: **Cursor**, **Claude Code**, **Antigravity**, entre outras — sem necessidade de reconfiguração.

---

## Pontos Fortes
*   **Escalabilidade:** Permite que IAs desenvolvam sistemas grandes e complexos sem perder contexto.
*   **Prevenção de "Spaghetti Code":** O planejamento arquitetural obrigatório antes do código eleva significativamente a qualidade.
*   **Agnóstico de Ferramenta:** Pode ser usado com Claude Code, Cursor, Codex, Antigravity, ou qualquer ferramenta que suporte arquivos de contexto.
*   **Gratuito e Open Source:** Sem custos de licenciamento.

---

## Casos de Uso
*   Construção de plataformas SaaS do zero com rastreabilidade completa.
*   Equipes que desejam padronizar o uso de IA entre desenvolvedores.
*   Refatorações de sistemas onde regras de negócio não podem ser perdidas.
*   Projetos enterprise com requisitos de compliance e auditoria.

---

## Links Úteis
*   **Site Oficial:** [https://www.bmad.dev/](https://www.bmad.dev/)
