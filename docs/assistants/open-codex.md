# Open Codex

> [!NOTE]
> O Open Codex é uma alternativa open-source comunitária ao ecossistema fechado de assistentes CLI proprietários, projetada para ser leve, transparente, focada em segurança local e 100% agnóstica de provedor de IA.

## Visão Geral
O **Open Codex** é um agente de codificação de código aberto para terminal (*terminal-first*), criado originalmente como fork comunitário e modernizado para suportar a nova geração de provedores de IA. Ele permite que desenvolvedores operem de forma independente de plataformas proprietárias, alternando livremente entre APIs comerciais de ponta e modelos locais de código aberto rodando via Ollama ou vLLM.

## Principais Funcionalidades e Novidades (2025–2026)
- **CLI Interativa e Modo Full Auto:**
  - Modo interativo padrão com aprovação de diffs e comandos passo a passo.
  - Modo autônomo (*Full Auto*): diagnóstico iterativo, aplicação de modificações e execução de testes em loop contínuo até sanar os erros encontrados.
- **Prompting Modular Baseado em Arquivos:**
  - Suporte automático a regras de projeto via `codex.md` (no repositório) e regras globais de usuário via `~/.codex/instructions.md`.
- **Agnosticismo Total de Provedores:**
  - Compatibilidade com endpoints no padrão OpenAI Chat Completions, suportando OpenAI, Anthropic, Google Gemini, OpenRouter, Mistral, Groq e instâncias locais (Ollama, vLLM, LM Studio).
- **Sandboxing e Isolamento de Segurança:**
  - Capacidade de executar comandos e modificações em ambientes isolados utilizando contêineres Docker ou Seatbelt no macOS/Linux, prevenindo chamadas não autorizadas de rede e alterações fora do diretório de trabalho.
- **Execução Headless para CI/CD:**
  - Modo não-interativo com saídas padronizadas em JSON para integração em GitHub Actions, GitLab CI e pipelines automatizados de lint e testes.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Zero Vendor Lock-in:** Liberdade total para trocar modelos conforme custo, latência ou privacidade.
- **Custo Zero em Modo Local:** Ao parear com modelos abertos locais (ex: DeepSeek-Coder, Llama), opera com custo financeiro nulo e sem envio de código para a nuvem.
- **Leveza e Transparência:** Código enxuto, sem telemetria oculta, permitindo auditoria completa.

### Limitações
- **Dependência da Capacidade do Modelo Escolhido:** Modelos menores locais podem apresentar alucinações sintáticas em linguagens menos populares.
- **Ausência de Interface Gráfica:** Voltado exclusivamente a usuários confortáveis com linha de comando.

## Casos de Uso
- Ambientes corporativos com restrições rígidas de privacidade que exigem modelos locais e air-gapped.
- Pipelines de CI/CD para auto-fix de linting, formatação e resolução de testes unitários quebrados.
- Alternativa econômica e flexível para desenvolvedores independentes e estudantes.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT).
- **Preço:** Totalmente gratuito e de código aberto; custos associados limitam-se ao consumo de APIs externas (quando utilizadas).
- **Agnóstico de Provedor:** Sim (100% agnóstico).

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/ymichael/open-codex](https://github.com/ymichael/open-codex)
