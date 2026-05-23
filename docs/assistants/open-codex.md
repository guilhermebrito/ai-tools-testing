# Open Codex

> [!NOTE]
> O Open Codex é um **fork comunitário leve** do Codex CLI oficial da OpenAI, focado em **agnósticismo de provedor** e execução local segura. Não deve ser confundido com a plataforma oficial OpenAI Codex.

## Visão Geral
O [Open Codex](https://github.com/ymichael/open-codex) é um agente de codificação open-source e leve que roda no terminal. Criado como um *fork* modificado da ferramenta original de CLI da OpenAI, ele foi adaptado para suportar o ecossistema moderno e diversificado de provedores de Inteligência Artificial, permitindo que desenvolvedores usem modelos gratuitos, locais ou de terceiros como alternativa às APIs proprietárias.

---

## Como Funciona

*   **Instalação:** Via npm (`npm i -g open-codex`), funciona recebendo comandos diretos ou rodando no modo "Full Auto", onde itera no código por conta própria.
*   **Chat Completions API:** Comunica-se usando a API padrão de Chat Completions, o que permite substituir o endpoint da OpenAI por qualquer provedor compatível.
*   **Arquivos de Contexto:** Assimila contexto lendo arquivos globais (`~/.codex/instructions.md`) e locais do projeto (`codex.md`).

---

## Pontos Fortes

*   **Agnóstico de Provedor:** Funciona nativamente com **OpenAI**, **Google Gemini**, **OpenRouter** e ferramentas locais como **Ollama** — ideal para quem busca a experiência do Claude Code ou Codex sem depender de APIs pagas.
*   **Foco em Segurança (Sandboxing):** Roda comandos localmente bloqueando tráfego de rede e isolando diretórios (usando *Apple Seatbelt* no macOS e *Docker* no Linux).
*   **Integração Contínua (CI):** Possui modo *Non-interactive* (`-q`), sendo excelente para rodar em pipelines como GitHub Actions para gerar changelogs ou aplicar correções triviais automaticamente.
*   **Leveza:** Foco em ser uma alternativa leve e modular, sem a complexidade de plataformas enterprise.

---

## Status e Posicionamento
O Open Codex é mantido pela comunidade e não possui o mesmo ciclo de releases agressivo de ferramentas comerciais. Ele permanece como uma alternativa prática para desenvolvedores que priorizam **controle local**, **privacidade** e **custo zero** (via Ollama ou modelos locais).

---

## Casos de Uso
*   Desenvolvedores de terminal que buscam uma experiência agentic usando modelos gratuitos locais (Ollama) ou via OpenRouter.
*   Automação segura de tarefas em pipelines CI/CD com modo não-interativo.
*   Prototipagem e scripts rápidos sem custos de API.

---

## Links Úteis
*   **Repositório Oficial (GitHub):** [https://github.com/ymichael/open-codex](https://github.com/ymichael/open-codex)
