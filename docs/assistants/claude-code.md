# Claude Code

> [!NOTE]
> Claude Code evoluiu de um simples assistente CLI para uma **plataforma agentic completa**, com extensões nativas para IDEs, sistema de plugins, orquestração multi-agente e execução remota.

## Visão Geral
O **Claude Code** é a ferramenta oficial de desenvolvimento de software da **Anthropic**, alimentada pela família de modelos Claude (incluindo **Claude Sonnet 4.6**, **Opus 4.6** e **Opus 4.7** em "Fast Mode"). Originalmente concebido como um agente de terminal puro, ele expandiu-se em 2026 para cobrir múltiplas superfícies (CLI, IDE e painel de agentes), mantendo a filosofia *terminal-first* como base.

---

## Interfaces Disponíveis

*   **CLI (Terminal):** A interface original e principal. O Claude Code vive no terminal, lê arquivos, aplica modificações e executa comandos de shell diretamente, com suporte a janelas de contexto de até **1 milhão de tokens**.
*   **Extensões IDE (VS Code & JetBrains):** Extensões nativas para **VS Code** (incluindo forks como Cursor, Windsurf e Kiro) e **JetBrains** (IntelliJ, PyCharm, etc.). Proporcionam visualização de diffs integrada no editor, compartilhamento automático de contexto (arquivos abertos, seleções, erros de lint) e atalhos rápidos (`Cmd+Esc`).
*   **Agent View (Research Preview):** Um painel centralizado para gerenciar múltiplas sessões paralelas do Claude Code, permitindo monitorar tarefas em execução, sessões bloqueadas por input e trabalhos concluídos em uma única tela.

---

## Funcionalidades e Recursos (2026)

### Autonomia e Execução
*   **Goal Mode (`/goal`):** Define uma condição de conclusão (ex: "até que todos os testes em `test/auth` passem") e o Claude trabalha continuamente sem necessidade de prompts manuais até atingir o objetivo.
*   **Auto Mode & Permissions:** Um classificador de segurança baseado em IA avalia automaticamente se chamadas de ferramentas são seguras, reduzindo drasticamente a necessidade de aprovações manuais repetitivas.
*   **Routines:** Automações reutilizáveis (prompt + repositório + ferramentas) que podem ser disparadas por agendamentos, webhooks ou eventos do GitHub (ex: preparação de PRs durante a noite).
*   **Remote Control:** Permite iniciar uma sessão na máquina local e retomá-la remotamente via interface mobile ou web, ideal para tarefas de longa duração.

### Extensibilidade
*   **Hooks:** Automatizam ações em pontos específicos do fluxo de trabalho (ex: rodar linter antes de commit, executar testes após alterações).
*   **Plugins:** Arquitetura de plugins carregáveis via `--plugin-dir` ou `--plugin-url` (suporte a arquivos `.zip`), com um marketplace crescente para especializações em diferentes indústrias.
*   **Claude Agent SDK:** SDK para construir agentes customizados com acesso às mesmas ferramentas, memória e frameworks de permissões do Claude Code, incluindo orquestração multi-agente com delegação de tarefas para subagentes especialistas.
*   **Tool Search:** Camada de indireção que permite ao Claude acessar bibliotecas amplas de ferramentas sem sobrecarregar a janela de contexto.

---

## Pontos Fortes
*   **Raciocínio Excepcional:** A profundidade do raciocínio lógico do Claude (especialmente com Opus 4.6/4.7) o torna excelente para refatorações complexas e debugging avançado.
*   **Contexto Ultra-Longo (1M tokens):** Capacidade de absorver bases de código inteiras para tomar decisões assertivas com visão global do projeto.
*   **Ecossistema Completo:** Da CLI ao painel de agentes, passando por extensões IDE e SDK, cobre todo o espectro de necessidades do desenvolvedor.

---

## Casos de Uso
*   Auditoria e refatoração de projetos legados com contexto completo do repositório.
*   Execução autônoma de objetivos complexos via Goal Mode (ex: migrar biblioteca de UI inteira).
*   Automação de fluxos de CI/CD com Routines (preparação de PRs, changelogs noturnos).
*   Orquestração multi-agente via Agent SDK para times de IA especializados.

---

## Acesso e Preços
*   **Plano Pro / Max / Team / Enterprise:** Acesso via assinatura Anthropic com limites de rate variáveis (recentemente dobrados para todos os planos pagos).
*   **API Direta:** Requer chave de API da Anthropic. Sem plano gratuito standalone.

---

## Links Úteis
*   **Documentação Oficial:** [https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
*   **Repositório (NPM):** [https://www.npmjs.com/package/@anthropic-ai/claude-code](https://www.npmjs.com/package/@anthropic-ai/claude-code)
