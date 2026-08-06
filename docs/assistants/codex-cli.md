# Codex CLI / Copilot CLI

## Visão Geral
Refere-se à categoria clássica de ferramentas de linha de comando alimentadas por IA (como o GitHub Copilot in the CLI ou wrappers originais do OpenAI Codex). Seu propósito principal é traduzir descrições em linguagem natural para comandos executáveis de shell.

## Principais Funcionalidades / Como Funciona
- **Tradução Linguagem Natural para Shell:** Você descreve o que quer fazer (ex: `?? find all typescript files modified today and list their sizes`) e ele gera o comando Bash correspondente.
- **Explicação de Comandos:** Geralmente retorna uma explicação didática do que cada parâmetro e *flag* faz.
- **Validação de Execução:** Pede confirmação explícita antes de rodar os comandos gerados.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Acelera Tarefas DevOps:** Elimina a necessidade de memorizar sintaxes obscuras de ferramentas como `awk`, `sed`, `tar` ou CLI da AWS/Docker.
- **Excelente Fator Didático:** Ajuda novos desenvolvedores a aprenderem e dominarem o terminal de forma prática.

### Limitações
- Ferramentas de "um único turno": não possuem memória profunda ou habilidade de gerenciar o contexto do código fonte inteiro.
- Estritamente limitadas à geração de comandos de terminal, sem capacidade de editar múltiplos arquivos de código autonomamente.

## Casos de Uso
- Administração de sistemas e gestão de infraestrutura (Linux/Mac).
- Manipulação rápida e tratamento de logs e dados tabulares (CSV) via bash.
- Operações de Git complexas (ex: rebases interativos difíceis).

## Status, Preço e Licenciamento
- **Modelo:** Misto (O GitHub Copilot CLI é proprietário, mas existem alternativas baseadas em scripts open-source).
- **Preço:** O Copilot CLI requer a assinatura do GitHub Copilot. Alternativas dependem do provedor de API utilizado.
- **Agnóstico de Provedor:** Geralmente Não (Atrelado ao ecossistema da OpenAI / Microsoft).

## Links Úteis
- **GitHub Copilot CLI:** [https://docs.github.com/en/copilot/github-copilot-in-the-cli](https://docs.github.com/en/copilot/github-copilot-in-the-cli)
- **OpenAI Codex:** [https://openai.com/index/openai-codex/](https://openai.com/index/openai-codex/)
