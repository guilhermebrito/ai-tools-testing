# Open Codex

## Visão Geral
O [Open Codex](https://github.com/ymichael/open-codex) é um agente de codificação leve e open-source que roda no terminal. Ele é um *fork* turbinado da ferramenta original de CLI da OpenAI, modificado para suportar o ecossistema moderno de provedores de Inteligência Artificial.

## Como Funciona
- Instalado via npm (`npm i -g open-codex`), ele funciona recebendo comandos diretos ou rodando no modo "Full Auto", onde ele itera no código por conta própria.
- Ele se comunica usando a *Chat Completions API*, o que permite substituir o endpoint da OpenAI por qualquer outro compatível.
- Ele assimila contexto lendo arquivos globais (`~/.codex/instructions.md`) e locais do projeto (`codex.md`).

## Pontos Fortes
- **Agnóstico de Provedor:** Funciona nativamente com OpenAI, Google Gemini, OpenRouter e ferramentas locais como Ollama.
- **Foco em Segurança (Sandboxing):** Ele roda comandos localmente bloqueando tráfego de rede e isolando diretórios (usando *Apple Seatbelt* no Mac e *Docker* no Linux).
- **Integração Contínua (CI):** Possui um modo *Non-interactive* (`-q`), sendo excelente para rodar em pipelines (como GitHub Actions) para gerar *Changelogs* ou aplicar correções triviais automaticamente.

## Casos de Uso
- Desenvolvedores de terminal que buscam a experiência do *Claude Code*, mas usando modelos gratuitos locais (Ollama) ou OpenRouter.
- Automação segura de tarefas em pipelines CI/CD.

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/ymichael/open-codex](https://github.com/ymichael/open-codex)
