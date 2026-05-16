# Codex CLI / Copilot CLI

## Visão Geral
Refere-se à categoria de ferramentas de linha de comando alimentadas por IA (como o GitHub Copilot in the CLI ou wrappers open-source do OpenAI Codex) projetadas para traduzir linguagem natural em comandos executáveis de shell.

## Como Funciona
Em vez de buscar no Google ou no StackOverflow como escrever um comando complexo no Linux/Mac, o usuário digita algo como:
`?? find all typescript files modified in the last 24 hours and list their sizes`

A IA retorna o comando exato (ex: `find . -name "*.ts" -mtime -1 -exec ls -lh {} +`), muitas vezes explicando o que cada flag faz e pedindo confirmação antes de executar.

## Pontos Fortes
- **Agilidade em DevOps:** Reduz a necessidade de memorizar sintaxes complexas de ferramentas como `find`, `grep`, `awk`, `tar`, ou Docker/Git.
- **Didática:** Ajuda a aprender linha de comando, pois frequentemente explica a solução sugerida.

## Casos de Uso
- Administração de sistemas locais ou remotos via SSH.
- Manipulação e tratamento rápido de arquivos (logs, CSVs).
- Operações de Git complexas (rebases, cherry-picks).
