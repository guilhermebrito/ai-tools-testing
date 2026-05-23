# Paperclip

## Visão Geral
Paperclip é uma plataforma open-source de orquestração UI-driven para agentes de Inteligência Artificial. Diferente de um agente de código tradicional, o Paperclip age como a "Empresa" ou o "Painel de Controle" que gerencia esses agentes.

## Como Funciona
- **Bring-Your-Own-Agent (BYOA):** O Paperclip não se importa com qual agente você usa (pode ser um script Bash, o Claude Code, ou um script Python simples).
- **Heartbeats & Filas:** A plataforma atribui tarefas para os agentes e fica enviando "heartbeats" (sinais vitais) para garantir que eles trabalhem nas filas de forma contínua e autônoma, 24/7.
- **Gestão de Orçamento:** Permite definir limites de gastos de tokens/API para que um agente em loop não consuma todo o cartão de crédito.

## Pontos Fortes
- **Resolução do Problema "Stateless":** Garante que os agentes mantenham memória e contexto entre sessões. Se a máquina reiniciar, o agente volta de onde parou.
- **Orquestração Visual:** Fornece um dashboard para ver quem (qual agente) está fazendo o que, e aprovar o trabalho antes de fazer merge.

## Casos de Uso
- Operar uma empresa orientada por IA, onde você tem múltiplos agentes assumindo papéis de marketing, pesquisa, QA e desenvolvimento em paralelo.
- Automação de tarefas longas de infraestrutura que demoram dias para concluir.

## Links Úteis
- **Site Oficial:** [https://paperclip.dev/](https://paperclip.dev/)
- **Repositório Oficial (GitHub):** [https://github.com/paperclip-dev/paperclip](https://github.com/paperclip-dev/paperclip)
