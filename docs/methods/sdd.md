# SDD (Spec-Driven Development)

> [!NOTE]
> O **Spec-Driven Development (SDD)** é um paradigma de engenharia de software onde a **especificação técnica estruturada** — e não o chat ad-hoc com o modelo ou o código prévio — atua como a fonte única da verdade (*Single Source of Truth*). O SDD consolida-se como a principal resposta metodológica contra o "vibe coding", garantindo que agentes e assistentes de IA operem sob contratos arquiteturais claros, critérios de aceitação rígidos e ciclos de verificação fechada.

---

## Visão Geral
À medida que os modelos de IA tornaram-se mais potentes (como Claude 3.7/4.5, GPT-5/o3 e Gemini 2.5 Pro), a velocidade de geração de código aumentou exponencialmente. No entanto, o desenvolvimento baseado em tentativa-e-erro e prompts conversacionais livres (*vibe coding*) gerou gargalos críticos: dívida técnica oculta, inconsistências arquiteturais, perda de contexto e dificuldade de manutenção em bases de larga escala.

O **SDD** propõe inverter essa dinâmica: antes que qualquer linha de código seja gerada ou editada por uma IA, o time (humano ou com auxílio de IA) elabora e aprova especificações determinísticas em arquivos versionados no repositório (geralmente Markdown, JSON Schemas ou OpenAPI). A IA deixa de "adivinhar" requisitos e passa a agir como um compilador e executor de especificações formais.

---

## Pilares Fundamentais do SDD

1. **Especificação como Fonte Única da Verdade:**
   - Nenhuma decisão de regra de negócio, contrato de dados ou limite arquitetural vive exclusivamente no contexto volátil do chat. Toda definição reside em artefatos versionáveis (ex: `specs/`, `.rules`, `PRDs`).

2. **Decomposição em Contratos e Casos de Borda:**
   - Antes da implementação, a especificação delimita explicitamente modelos de dados, endpoints, estados de erro e critérios de aceitação testáveis (Gherkin/BDD ou suítes de teste antecipadas).

3. **Injeção Cirúrgica de Contexto (Context Window Management):**
   - Agentes de código recebem apenas o fragmento exato da especificação e o código relevante para a tarefa atual, minimizando ruído, custos de tokens e alucinações.

4. **Verificação de Ciclo Fechado (Closed-Loop Verification):**
   - O código gerado pela IA é automaticamente checado e validado contra os critérios de aceitação estipulados na especificação antes de ser integrado ao fluxo Git principal.

---

## Níveis de Maturidade na Adoção do SDD

O mercado e a literatura categorizam a maturidade do SDD em três níveis progressivos:

1. **Nível 1 — Spec-First (Planejamento Antecipado):**
   - O desenvolvedor redige uma especificação formal antes de solicitar código ao assistente. O documento atua como um guia estruturado de prompt, mas a sincronização durante mudanças ainda é predominantemente manual.
2. **Nível 2 — Spec-Anchored (Especificação Viva / Âncora):**
   - A especificação é tratada como um documento vivo integrado à ferramenta. Agentes e humanos utilizam comandos de sincronização contínua (ex: `/sync`) para garantir que o código e a especificação evoluam juntos, prevenindo o *spec drift*.
3. **Nível 3 — Spec-as-Source (Especificação como Código Primário):**
   - A especificação é o artefato central soberano. O código, os testes e os diagramas são derivados automáticos gerados por agentes e validados por suítes de verificação formal a cada alteração na especificação.

---

## Ciclo de Vida Operacional do SDD (Pipeline Canônico)

Na prática, o fluxo de desenvolvimento guiado por especificações segue 6 etapas sequenciais:

```
┌─────────────────┐     ┌──────────────┐     ┌──────────────────┐
│  Constitution   │ ──> │   Specify    │ ──> │ Plan & Contracts │
│ (Regras Globais)│     │  (Intenção)  │     │  (Arquitetura)   │
└─────────────────┘     └──────────────┘     └──────────────────┘
                                                       │
                                                       ▼
┌─────────────────┐     ┌──────────────┐     ┌──────────────────┐
│  Living Sync    │ <── │ Closed-Loop  │ <── │  Task Sharding   │
│  (Merge & Docs) │     │ Verification │     │  & Code Execution│
└─────────────────┘     └──────────────┘     └──────────────────┘
```

1. **Constituição & Governança Global (`constitution.md` / `.cursorrules`):**
   - Estabelece as regras imutáveis do repositório: stack tecnológico, convenções de código, diretrizes de segurança e restrições de arquitetura que nenhum agente pode violar.
2. **Elicitação e Intenção (`Specify`):**
   - Formalização do *problema de negócio* e das histórias de usuário, com foco no **"o quê"** e **"por quê"**, evitando detalhes de implementação prematuros.
3. **Planejamento Técnico e Contratos (`Plan & Contracts`):**
   - Definição dos modelos de domínio, esquemas de validação (JSON Schema, Zod, OpenAPI), fluxos assíncronos e critérios de aceite inequívocos.
4. **Fragmentação de Tarefas (`Task Sharding`):**
   - Decomposição do plano em tarefas atômicas e isoladas (geralmente arquivos de tarefas com escopo limitado), garantindo que a janela de contexto do agente não seja sobrecarregada.
5. **Execução Cirúrgica por Agentes (`Implement`):**
   - Assistentes e agentes (Cursor, Claude Code, Antigravity) recebem estritamente a sub-tarefa e os contratos relevantes, gerando código e testes unitários.
6. **Verificação de Ciclo Fechado & Sincronização (`Verify & Sync`):**
   - Validação automatizada do código contra os critérios da especificação. Se regras mudaram durante a execução, a especificação é sincronizada antes da abertura do Pull Request.

---

## Opções Derivadas e Variantes no Mercado

A partir dos princípios fundamentais do SDD, surgiram diferentes frameworks, toolkits e metodologias especializadas:

### 1. GitHub Spec Kit
* **O que é:** Toolkit open-source com CLI (`specify`) projetado para guiar agentes em um pipeline disciplinado: `constitution` $\rightarrow$ `specify` $\rightarrow$ `plan` $\rightarrow$ `tasks` $\rightarrow$ `implement`.
* **Foco:** Governança corporativa, conformidade rígida e integração nativa com o ecossistema GitHub/Copilot.
* **Perfil:** Alta cerimônia e rigor, ideal para grandes equipes e projetos de alta criticidade.

### 2. OpenSpec
* **O que é:** Framework ágil e minimalista focado em manter uma "Living Spec" (especificação viva) no próprio repositório Git.
* **Foco:** Agilidade com baixo atrito, utilizando comandos/skills padronizados (como `/opsx:propose`, `/opsx:apply` e `/opsx:sync`).
* **Perfil:** Mais leve que o Spec Kit, preferido por desenvolvedores individuais e times pequenos que querem governança sem excesso de arquivos intermediários.

### 3. BMAD (Breakthrough Method for Agile AI-Driven Development)
* **O que é:** Metodologia ágil que simula uma equipe completa de especialistas em IA (Analyst, PM, Architect, Developer, QA, Security, Data).
* **Foco:** Traduzir os artefatos do SDD em dinâmicas de cerimônias ágeis e transições de fase com validações automatizadas (*gating*).
* **Perfil:** Modelo operacional completo que responde ao **"como uma equipe de IA deve trabalhar"** em cima das especificações.

### 4. Traycer AI
* **O que é:** Camada visual de orquestração e governança spec-first que atua a montante de IDEs como Cursor e Claude Code.
* **Foco:** Editor visual de especificações (Visual Spec Editor), verificação automática antes de PRs e rastreabilidade total vinculada a Issues e PRs no GitHub.
* **Perfil:** Plataforma colaborativa amigável tanto para desenvolvedores quanto para PMs e designers.

### 5. Kiro & CodeMySpec
* **O que é:** Ferramentas focadas na reconciliação contínua entre documentos de design arquitetural e a base de código implementada.
* **Foco:** Mapeamento componente-a-requisito e detecção precoce de lacunas (*spec-to-code gap*).

---

## Matriz Comparativa: Derivações do SDD

| Solução / Variante | Categoria | Grau de Cerimônia | Artefatos Principais | Ideal Para |
| :--- | :--- | :---: | :--- | :--- |
| **GitHub Spec Kit** | Toolkit CLI Open-Source | Alto | `constitution.md`, `spec.md`, `plan.md`, `tasks.md` | Grandes empresas, auditoria formal, ecossistema GitHub |
| **OpenSpec** | Framework Leve / Skills | Médio | Especificação unificada viva (`openspec/`), `/opsx` | Equipes ágeis, fluxos interativos no terminal/IDE |
| **BMAD** | Metodologia de Agentes | Alto | PRDs, Arquitetura, Story Files, Personas Virtuais | Projetos complexos executados por múltiplos agentes |
| **Traycer AI** | Plataforma / Orquestrador | Médio | Visual Specs, Milestones, Verification Dashboard | Times híbridos (PM + Devs), handoff multi-ferramenta |
| **Kiro / CodeMySpec** | Ferramentas de Design Sync | Baixo a Médio | Design Documents, Component Maps | Prevenção de desvio arquitetural em microsserviços |

---

## SDD vs. BMAD: Resumo da Relação

```
┌──────────────────────────────────────────────────────────────┐
│                SDD (Spec-Driven Development)                 │
│              "A Filosofia / A Planta Baixa"                  │
│   Define a especificação e os contratos como fonte da verdade│
└──────────────────────────────┬───────────────────────────────┘
                               │
                implementado e operacionalizado por
                               │
                               ▼
┌──────────────────────────────────────────────────────────────┐
│                             BMAD                             │
│               "O Modelo Operacional / A Linha"               │
│    Orquestra papéis (PM, Architect, Dev, QA) e cerimônias    │
│            para transformar a spec em software real          │
└──────────────────────────────────────────────────────────────┘
```

---

## Boas Práticas e Anti-Padrões

### Boas Práticas
- **Spec Sharding (Fragmentação):** Nunca envie uma especificação monolítica inteira para o agente. Divida em módulos atômicos que caibam confortavelmente na janela de atenção da IA.
- **Sync ao Fechar Sessões:** Atualize a especificação ao final de cada iteração de código para evitar o temido *Spec Drift* (quando o código funciona mas a documentação mente).
- **Testes Baseados em Contratos:** Gere casos de teste unitários e de integração derivados diretamente da especificação antes que a implementação seja iniciada.

### Anti-Padrões a Evitar
- **Spec Vaga:** Textos genéricos ("criar um sistema rápido e bonito") forçam o agente a alucinar, revertendo o processo ao *vibe coding*.
- **Over-Specification de Implementação:** Tentar especificar cada linha de código ou sintaxe exata na spec remove a utilidade da IA e burocratiza o desenvolvimento. O foco da spec deve ser **comportamento, limites e contratos**.
- **Spec Abandonada:** Alterar código diretamente sem atualizar a spec transforma a documentação em dívida técnica.

---

## Status e Licenciamento
- **Modelo:** Paradigma Aberto de Engenharia de Software.
- **Preço:** Conceito livre (implementável via Markdown puro ou com ferramentas pagas/open-source).
- **Agnóstico de Provedor:** 100% agnóstico de ferramentas, LLMs e ambientes de desenvolvimento.
