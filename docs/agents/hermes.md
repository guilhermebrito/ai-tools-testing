# Hermes (Nous Research)

> [!NOTE]
> O Hermes é um agente **auto-evolutivo**: ele resolve problemas, cria "Skills" documentadas sobre como resolvê-los, e as refina automaticamente ao longo do tempo — ficando mais rápido e preciso a cada tarefa.

## Visão Geral
Desenvolvido pela **Nous Research**, o **Hermes** é um agente de IA open-source altamente capaz, desenhado para atuar como um **assistente pessoal persistente** focado em desenvolvedores. Instalável via script oficial ou `pip install hermes-agent`, ele opera como um orquestrador de terminal com loop de aprendizado contínuo e suporte a mais de **5 plataformas de mensageria** (Telegram, Discord, Slack, WhatsApp, Signal).

---

## Funcionalidades e Recursos (v0.15.1 · Maio 2026)

### Sistema de Skills (Auto-Aperfeiçoamento)
*   **Criação de Skills:** Quando resolve um problema complexo, o Hermes escreve uma "Skill" (documento Markdown) detalhando a solução. No futuro, consulta essas skills para resolver problemas similares de forma mais rápida e precisa.
*   **90+ Skills Bundled:** A instalação já inclui skills pré-criadas cobrindo desde MLOps (`dspy`, `serving-llms-vllm`, `weights-and-biases`) até automação criativa (`ascii-art`, `manim-video`, `pixel-art`), GitHub (`github-pr-workflow`, `github-code-review`) e produtividade (`notion`, `google-workspace`, `obsidian`).
*   **Auto-Evolução (Experimental):** Recursos como `hermes-agent-self-evolution` utilizam DSPy e GEPA para **reescrever e otimizar automaticamente** os arquivos de skills com base em traces de execução.
*   **Community Hub:** Browse e instalação de skills da comunidade via `agentskills.io` com um único comando.

### Orquestração Multi-Agente (Kanban)
*   **Kanban Board Durável:** Sistema de delegação de tarefas para times de agentes com monitoramento por heartbeat, detecção de tarefas "zumbi", retries automáticos e recuperação de alucinações.
*   **Sub-agentes Paralelos:** Spawn de agentes isolados para workstreams paralelos, cada um com conversa e terminal próprios.

### Automação e Computer Use
*   **Computer Use Universal:** Driver de interação com a interface gráfica (screenshots, cliques, inputs de teclado) compatível com múltiplos modelos.
*   **Browser Automation:** Automação de navegador via Playwright/Chrome, incluindo busca web, extração de conteúdo e controle full de UI.
*   **Tool Gateway:** Gateway integrado para web search (Brave, DuckDuckGo, Exa, Tavily), geração de imagens, text-to-speech e automação avançada de navegador.

### MLOps & Training Data
*   **Batch Processing:** Geração de milhares de trajetórias de tool-calling em paralelo com checkpointing automático.
*   **RL Training:** Integração com Atropos para reinforcement learning em comportamentos agênticos.
*   **Trajectory Export:** Exportação de conversas em formato ShareGPT para fine-tuning.

### Conectividade
*   **5 Plataformas de Mensageria:** Telegram, Discord, Slack, WhatsApp e Signal — tudo a partir de um único processo gateway.
*   **Suporte Mobile:** Operação nativa em Android via Termux.
*   **Session Handoff:** Transferência de sessões ativas entre plataformas de forma transparente.
*   **Agendamento Cron:** Agendador integrado com entrega em qualquer plataforma configurada.

### Performance (v0.15.1)
*   **Agent Loop 47% mais rápido** (v0.14.0+): Otimizações no hot-path de execução.
*   **Cold Start reduzido:** Inicialização mais rápida com `uv` como gerenciador de pacotes.
*   **LSP Diagnostics:** Erros de language server em tempo real diretamente no workspace do agente.
*   **Instalação Nativa macOS/Linux:** Sem necessidade de WSL2 (Windows em modo experimental).

---

## Experiência de Instalação (macOS, Maio 2026)

### Método Recomendado: Script Oficial

```bash
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

O script provisiona **todas as dependências automaticamente**, sem necessidade de `sudo`:

| Dependência | Versão instalada | Observação |
|:---|:---|:---|
| Python | 3.11.15 | Via `uv` |
| Hermes Agent | 0.15.1 | `hermes-agent==0.15.1` |
| OpenAI SDK | 2.24.0 | Compatível com qualquer endpoint |
| Node.js | ✓ | Para browser tools |
| Playwright/Chromium | ✓ | Detecta Chrome do sistema automaticamente |
| ripgrep | ✓ | Busca de arquivos mais rápida |
| docker | ✓ | Ambientes isolados (opcional) |

**Tempo total de instalação:** ~3–5 minutos em conexão boa (inclui download de 101 pacotes Python + build da extensão do Node.js).

> [!TIP]
> O instalador detectou automaticamente o **Google Chrome** instalado no sistema (`/Applications/Google Chrome.app`) e configurou o Playwright para usá-lo — pulando o download do Chromium bundled (~130 MB economizados).

### Estrutura de Arquivos Criada

```
~/.hermes/
├── .env                # API keys (OpenRouter, Telegram, etc.)
├── config.yaml         # Configuração principal (modelo, UI, hooks, etc.)
├── SOUL.md             # Persona e instruções de comportamento do agente
├── skills/             # 90 skills bundled (+ skills criadas pelo agente)
├── memories/           # Memórias persistentes (MEMORY.md, USER.md)
├── sessions/           # Histórico de sessões
├── logs/               # Logs de execução
└── cron/               # Jobs agendados
~/.local/bin/hermes     # Launcher (adicionado ao PATH via ~/.zshrc)
```

---

## Configuração com OpenRouter

### Passo 1 — Configurar o Provedor

```bash
hermes config set model.provider openrouter
hermes config set model.default "google/gemini-2.0-flash-001"
```

### Passo 2 — Adicionar a API Key

Edite `~/.hermes/.env` e adicione/descomente:

```env
OPENROUTER_API_KEY=sk-or-v1-...
```

### Passo 3 — Verificar a Instalação

```bash
hermes doctor
```

**Resultado esperado:**

```
✓ OpenRouter API          ← conectividade confirmada
✓ browser                 ← automação de navegador
✓ terminal                ← execução de comandos
✓ file                    ← leitura/escrita de arquivos
✓ memory                  ← memória persistente
✓ skills                  ← sistema de skills
✓ vision                  ← análise de imagens
✓ delegation              ← orquestração de sub-agentes
```

> [!IMPORTANT]
> **Atenção ao `max_tokens`:** O modelo padrão do Hermes solicita até **64.000 tokens** de contexto por requisição. Modelos premium no OpenRouter (ex: `anthropic/claude-sonnet-4-5`) podem gerar erro 402 se o limite diário da chave for baixo. Use modelos free-tier como `google/gemini-2.0-flash-001` para testes iniciais, ou aumente o crédito diário em [openrouter.ai/settings/credits](https://openrouter.ai/settings/credits).

---

## Primeiros Passos

### Modo Interativo (TUI)

```bash
hermes          # Inicia o chat interativo com banner, spinner e tool previews
```

### Modo Query (Single-shot)

```bash
hermes chat -q "Qual é o estado atual do meu projeto?"
```

### Modo One-shot (saída limpa para scripts)

```bash
hermes -z "Resuma os últimos commits do git" 
```

### Comandos Essenciais

| Comando | Descrição |
|:---|:---|
| `hermes` | Inicia o chat interativo |
| `hermes chat -q "<prompt>"` | Envia uma única mensagem e exibe resposta |
| `hermes -z "<prompt>"` | One-shot: imprime só a resposta final (ideal para scripts) |
| `hermes --resume <session_id>` | Retoma uma sessão anterior pelo ID |
| `hermes -c` | Retoma a sessão mais recente |
| `hermes -c "nome"` | Retoma sessão por nome/título |
| `hermes model` | Troca interativamente de modelo/provedor |
| `hermes config set <key> <value>` | Altera configuração sem abrir o arquivo |
| `hermes skills list` | Lista todas as skills disponíveis |
| `hermes skills install <nome>` | Instala uma skill da comunidade |
| `hermes gateway setup` | Configura gateway de mensageria (Telegram/Discord/etc.) |
| `hermes update` | Atualiza para a versão mais recente |
| `hermes doctor` | Diagnóstico completo do ambiente |

### Comandos em Runtime (dentro do chat)

| Slash Command | Descrição |
|:---|:---|
| `/model <modelo>` | Troca o modelo na sessão atual |
| `/skin <nome>` | Muda o tema visual (default, ares, mono, slate, poseidon...) |
| `/reasoning show/hide` | Exibe ou oculta o raciocínio do modelo |
| `/reset` | Limpa o contexto da conversa atual |

---

## Comportamento Observado em Testes

### Ferramentas Ativas na Sessão

Durante as sessões de teste, o Hermes exibiu os tool calls em tempo real com prefixo `┊`, por exemplo:

```
┊ 📚 preparing skills_list…
┊ 📚 skills    list all  0.0s
┊ ✍️ preparing write_file…
┊ ✍️  write     /path/to/file.md  0.2s
┊ review diff
```

### Criação de Arquivo com Diff

O agente apresenta um diff visual antes de confirmar a escrita de qualquer arquivo:

```diff
a/arquivo.md → b/arquivo.md
@@ -0,0 +1,4 @@
+Linha adicionada 1
+Linha adicionada 2
```

### Gerenciamento de Sessões

Cada sessão recebe um ID automático no formato `YYYYMMDD_HHMMSS_<hash>`. Ao final de cada sessão, o Hermes imprime:

```
Resume this session with:
  hermes --resume 20260530_215017_697d01

Session:        20260530_215017_697d01
Duration:       5s
Messages:       4 (1 user, 2 tool calls)
```

---

## Pontos Fortes
*   **Privacidade e Self-Hosting:** Roda inteiramente em infraestrutura própria. Todos os dados ficam em `~/.hermes/` na sua máquina. Zero telemetria.
*   **Agnóstico de Modelo:** Suporta centenas de modelos — OpenAI, Anthropic, Google Gemini, xAI Grok, Ollama, LM Studio, qualquer endpoint compatível com a API OpenAI — sem alteração de código.
*   **Instalação Sem Atrito:** Um único `curl | bash` provisiona Python, Node.js, browser engine e 90 skills. Sem `sudo`, sem conflito com o Python do sistema.
*   **Aprendizado Contínuo:** O loop fechado de Skills garante melhoria progressiva com o uso.
*   **UX Rica no Terminal:** Banner colorido, spinner animado, diff de arquivos, temas (skins), streaming de tokens — experiência muito acima do padrão de ferramentas CLI.
*   **Sessões Persistentes e Retomáveis:** Cada conversa tem ID único e pode ser retomada a qualquer momento com `--resume`.
*   **Hooks de Shell:** Sistema de hooks (`pre_tool_call`, `post_tool_call`, etc.) permite integrar scripts externos para bloquear comandos perigosos ou auto-formatar código.

---

## Casos de Uso
*   Assistente pessoal permanente rodando em VPS privada ou máquina local.
*   Automação de CI/CD não-padrão e tarefas de infraestrutura.
*   Delegação de tarefas complexas e longas a partir de dispositivos móveis via chat (Telegram/WhatsApp).
*   Orquestração de times de agentes via Kanban para projetos de larga escala.
*   Geração de training data para fine-tuning de LLMs (batch processing + trajectory export).
*   Automações agendadas via cron com entrega de resultados por mensageria.

---

## Links Úteis
*   **Site Oficial:** [https://hermes-agent.org/](https://hermes-agent.org/)
*   **Nous Research:** [https://nousresearch.com/](https://nousresearch.com/)
*   **Repositório Oficial (GitHub):** [https://github.com/NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
*   **OpenRouter (Provedores de Modelos):** [https://openrouter.ai/](https://openrouter.ai/)
*   **Community Skills Hub:** [https://agentskills.io/](https://agentskills.io/)
