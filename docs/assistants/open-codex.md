# Open Codex

## Visão Geral
O Open Codex é um agente de codificação open-source focado inteiramente na interface de linha de comando. Ele surgiu como um *fork* turbinado das antigas ferramentas de CLI, atualizado para operar de forma totalmente independente e suportar o ecossistema moderno de provedores de IA.

## Principais Funcionalidades / Como Funciona
- **CLI Interativa e Autônoma:** Executável direto do terminal (`open-codex`). Inclui um modo "Full Auto", onde ele mesmo identifica o erro e roda as modificações iterativamente.
- **Prompting Modular via Arquivos:** Lê diretrizes de design e padrões de código através da detecção automática de arquivos `codex.md` no projeto e `~/.codex/instructions.md` no sistema global.
- **Interoperabilidade Total de APIs:** Usa a padronização do *Chat Completions*, aceitando requisições do OpenAI, Anthropic, Google, OpenRouter e Ollama perfeitamente.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Totalmente Agnóstico e Sem Custos Inerentes:** O desenvolvedor não fica preso a um provedor; usar modelos abertos (Llama, DeepSeek) localmente corta custos a zero.
- **Design Voltado a CI/CD:** O modo não-interativo da ferramenta permite uso trivial em *pipelines* automatizadas (GitHub Actions, GitLab CI).
- **Isolamento de Segurança:** Pode rodar comandos locais bloqueando tráfego de rede e uso indevido de diretórios host (usando Docker / Seatbelt).

### Limitações
- Modelos locais leves (Ollama) nem sempre alcançam o desempenho de codificação *zero-shot* exigido por algumas tarefas complexas.
- Ausência de interface gráfica (GUI), exigindo desenvoltura no terminal.

## Casos de Uso
- Desenvolvedores *budget-conscious* ou estudantes usando modelos gratuitos na sua máquina local via Ollama.
- Integração em automações e fluxos de Integração Contínua (geração de logs, correção de indentação, *lint fixes* automatizados).
- Sandboxing seguro para execução de códigos suspeitos ou experimentais.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT).
- **Preço:** Totalmente gratuito, com os custos limitados apenas às requisições da própria API de IA escolhida pelo usuário.
- **Agnóstico de Provedor:** Sim (100% Flexível).

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/ymichael/open-codex](https://github.com/ymichael/open-codex)
