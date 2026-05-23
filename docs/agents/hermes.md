# Hermes (Nous Research)

## Visão Geral
Desenvolvido pela Nous Research, Hermes é um agente de Inteligência Artificial open-source altamente capaz, desenhado para atuar como um assistente pessoal persistente e focado em desenvolvedores.

## Como Funciona
- **Sistema de "Skills":** O Hermes se destaca pela capacidade de **auto-aperfeiçoamento**. Quando ele resolve um problema complexo no seu ambiente local, ele escreve uma "Skill" (um documento em Markdown) detalhando como resolver aquilo. No futuro, ele consulta essas skills para resolver problemas similares mais rápido.
- **Orquestrador de Terminal:** Ele vive no CLI e pode executar scripts, modificar arquivos e delegar sub-tarefas para outros trabalhadores (como chamar o Claude Code para escrever uma função enquanto o Hermes gerencia o repositório).
- **Agnóstico:** Suporta provedores comerciais (OpenAI, Anthropic) e modelos locais (Ollama, LM Studio).

## Pontos Fortes
- **Privacidade e Self-Hosting:** Pode rodar inteiramente em infraestrutura própria, ideal para código fonte sensível.
- **Conectividade:** Possui integração (gateways) para Telegram, Discord, Email e Slack, permitindo que você envie um comando de voz no Telegram e o agente execute um deploy no seu servidor em casa.

## Casos de Uso
- Assistente pessoal permanente rodando em uma VPS privada ou máquina local.
- Automação de CI/CD não-padrão.
- Delegação de tarefas complexas e longas a partir de dispositivos móveis via chat (Telegram/WhatsApp).

## Links Úteis
- **Nous Research:** [https://nousresearch.com/](https://nousresearch.com/)
- **Repositório Oficial (GitHub):** [https://github.com/NousResearch/Hermes](https://github.com/NousResearch/Hermes)
