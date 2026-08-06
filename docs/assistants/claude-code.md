# Claude Code

## Visão Geral
Claude Code é o assistente de linha de comando (CLI) oficial desenvolvido pela Anthropic, projetado para operar alimentado pela família de modelos Claude (com destaque para o Claude 3.7 Sonnet). Ele atua como um assistente de codificação diretamente no terminal do desenvolvedor.

## Principais Funcionalidades / Como Funciona
- **Integração de Terminal:** Vive nativamente no terminal e pode ler arquivos, explorar diretórios e consumir logs de build de forma autônoma.
- **Modificações Diretas:** Sugere e aplica modificações *inline* diretamente nos arquivos do projeto.
- **Execução de Comandos:** Capacidade de rodar comandos de sistema (ex: `npm test`, `cargo build`) para compilar e validar se as mudanças foram bem-sucedidas.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Raciocínio Excepcional:** Aproveita as habilidades analíticas profundas do Claude, sendo excelente para refatorações extensas.
- **Gerenciamento de Contexto:** Pode analisar facilmente o código global do projeto.
- **Foco e Velocidade:** Ideal para desenvolvedores *terminal-first*, evitando que precisem trocar entre IDE, navegador e terminal.

### Limitações
- Restrito apenas aos modelos da Anthropic.
- O sistema de permissão (aprovação de comandos) pode atrasar a execução contínua totalmente autônoma.

## Casos de Uso
- Auditoria e refatoração de projetos legados pelo terminal.
- Análise de erros de build lendo diretamente a saída padrão.
- Criação rápida de *boilerplates* e scripts sem sair da CLI.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário.
- **Preço:** Instalação gratuita, porém pago sob demanda (consumo da API Anthropic).
- **Agnóstico de Provedor:** Não.

## Links Úteis
- **Site Oficial:** [https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- **Repositório (NPM):** [https://www.npmjs.com/package/@anthropic-ai/claude-code](https://www.npmjs.com/package/@anthropic-ai/claude-code)
