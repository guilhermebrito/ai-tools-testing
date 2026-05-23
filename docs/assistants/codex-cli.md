# OpenAI Codex

> [!NOTE]
> O Codex evoluiu de um simples modelo de code-completion para uma **plataforma agentic completa** com CLI, Desktop App, Goal Mode, sistema de plugins, Computer Use e agente de segurança dedicado.

## Visão Geral
O **OpenAI Codex** é a plataforma oficial de engenharia de software autônoma da **OpenAI**, alimentada por modelos de fronteira como o **GPT-5.5** (raciocínio complexo) e **GPT-5.4 mini** (roteamento eficiente de tarefas). Em 2026, a ferramenta transcendeu a categoria de "tradutor de linguagem natural para bash" para se tornar um sistema multi-superfície completo, capaz de planejar, executar e gerenciar fluxos de engenharia de software de ponta a ponta.

---

## Interfaces Disponíveis

*   **Codex CLI (`@openai/codex`):** Agente nativo de terminal para leitura de repositórios, edição de arquivos, execução de testes e commits — tudo diretamente do shell. Instalação via `npm i -g @openai/codex`.
*   **Codex Desktop App:** Aplicação desktop (macOS e Windows) que funciona como centro de comando com suporte a agentes paralelos, memória persistente de projeto e fluxos de trabalho integrados.

---

## Funcionalidades e Recursos (2026)

### Autonomia e Planejamento
*   **Goal Mode:** O agente trabalha orientado a objetivos de alto nível por períodos estendidos (horas ou dias), rastreando progresso entre turnos ativos sem necessidade de prompts manuais.
*   **Computer Use:** Capacidade nativa de interagir com interfaces gráficas — clicar, digitar e navegar em aplicações como um desenvolvedor humano faria.
*   **Appshots:** Permite enviar o contexto visual da janela ativa ou capturas de tela diretamente ao Codex como input contextual.

### Segurança e Sandboxing
*   **Codex Security (lançado março/2026):** Agente dedicado a segurança de aplicações que realiza threat modeling, scanning de vulnerabilidades e geração de patches em ambientes isolados (sandboxed).
*   **Controles Granulares:** Perfis de permissões configuráveis, controles de rede granulares e sandboxing avançado (bubblewrap/Docker) para execução segura e isolada.

### Extensibilidade
*   **Sistema de Plugins:** Conecta o Codex a toolchains de desenvolvimento como **Sentry**, **Datadog** e **Linear**.
*   **Suporte MCP:** Integração com servidores Model Context Protocol (MCP) com chamadas de ferramentas paralelas para maior eficiência.
*   **Triggers Automatizados:** Execução automática baseada em eventos do GitHub (PRs, issues, pushes).

---

## Pontos Fortes
*   **Agilidade em DevOps:** Elimina a necessidade de memorizar sintaxes complexas de ferramentas como `find`, `grep`, `awk`, `tar`, Docker e Git.
*   **Didática:** Explica os comandos sugeridos e pede confirmação antes de executar.
*   **Agentes Paralelos:** Suporte a múltiplos agentes trabalhando simultaneamente em diferentes partes do código.
*   **Segurança Integrada:** O Codex Security automatiza auditorias de segurança e geração de patches dentro de ambientes sandbox.

---

## Casos de Uso
*   Administração de sistemas e DevOps com tradução de linguagem natural para bash.
*   Engenharia autônoma de features completas via Goal Mode.
*   Auditorias de segurança automatizadas com Codex Security.
*   Integração em pipelines de CI/CD com triggers automáticos de GitHub.

---

## Acesso e Preços
*   **API Direta:** Requer chave de API da OpenAI. Sem plano gratuito standalone — custo baseado em tokens consumidos.
*   **ChatGPT Pro/Team/Enterprise:** Acesso integrado via assinatura OpenAI com limites de uso variáveis.

---

## Links Úteis
*   **OpenAI Codex:** [https://openai.com/index/openai-codex/](https://openai.com/index/openai-codex/)
*   **GitHub Copilot CLI:** [https://docs.github.com/en/copilot/github-copilot-in-the-cli](https://docs.github.com/en/copilot/github-copilot-in-the-cli)
*   **NPM:** [https://www.npmjs.com/package/@openai/codex](https://www.npmjs.com/package/@openai/codex)
