# OpenHands

> [!NOTE]
> O OpenHands (ex-OpenDevin) é a principal plataforma open-source de agentes autônomos de engenharia de software, com mais de **70k GitHub stars**, um Agent Control Plane para orquestração em escala e disponibilidade em SaaS (OpenHands Cloud).

## Visão Geral
O **OpenHands** (anteriormente OpenDevin) é uma plataforma open-source desenvolvida pela **All-Hands-AI** para atuar como um Engenheiro de Software de IA autônomo. Com $23.8M em financiamento total e uma comunidade extremamente ativa, ele se posiciona como a referência open-source para agentes de codificação capazes de explorar repositórios, planejar soluções, escrever código, rodar testes e iterar até a conclusão da tarefa.

---

## Funcionalidades Principais (2026)

### Autonomia e Planejamento
*   **Autonomia de Execução:** Capaz de explorar o repositório, planejar a solução, escrever código, rodar testes no terminal e iterar até que a tarefa seja concluída com sucesso.
*   **Planning Mode (Beta):** O agente cria um arquivo estruturado `PLAN.md` e solicita aprovação do usuário antes de executar alterações, permitindo validar a abordagem e escopo antes de tarefas complexas.

### Infraestrutura e Escala
*   **Agent Control Plane (maio/2026):** Plano de controle para gerenciar, monitorar e orquestrar agentes de software em escala organizacional — descrito como o "Kubernetes para agentes".
*   **Suporte Kubernetes:** Integração profunda com Kubernetes para execução paralela de agentes em larga escala em ambientes cloud-native.
*   **KVM Acceleration (`SANDBOX_KVM_ENABLED`):** Sandbox containers podem usar máquinas virtuais aceleradas por KVM em vez de emulação lenta, melhorando significativamente a performance de execução.

### Segurança e Isolamento
*   **Ambiente Sandboxed (Docker):** Utiliza containers Docker para criar um ambiente de trabalho seguro e isolado, onde o agente executa comandos CLI e compila código sem risco ao sistema host.
*   **Navegação Web:** Capacidade de abrir navegadores virtuais para pesquisar documentações, ler APIs e testar visualmente aplicações web construídas.

### Interface e UX
*   **GUI Slash Menu (`/`):** Menu integrado para descobrir e acessar rapidamente Agent Skills carregados.
*   **Indicador de Modelo Ativo:** A interface exibe o modelo LLM ativo em cartões de conversa e no header.
*   **OpenHands Cloud (SaaS):** Oferta gerenciada em nuvem para quem não deseja hospedar a infraestrutura localmente.

---

## Pontos Fortes
*   **Agnóstico de LLM:** Suporta Claude 4.5 Sonnet, GPT-4o, Gemini, Ollama, OpenRouter e modelos locais — sem vendor lock-in.
*   **Open Source (MIT):** Código completamente aberto, auditável e customizável.
*   **Enterprise Ready:** Posicionamento crescente para remediação automatizada de vulnerabilidades, modernização de código legado e integração em CI/CD.
*   **Comunidade Massiva:** 70k+ GitHub stars e ecossistema ativo de contribuidores.

---

## Casos de Uso
*   Resolução autônoma de Issues e correção de bugs em repositórios.
*   Criação de aplicações, scripts e automações end-to-end.
*   Exploração, documentação e refatoração de grandes bases de código legado.
*   Orquestração de agentes em escala organizacional via Agent Control Plane.

---

## Acesso e Preços
*   **Open Source (Self-Hosted):** Gratuito (Licença MIT). Requer chave de API própria para LLMs ou modelos locais.
*   **OpenHands Cloud (SaaS):** Oferta gerenciada em nuvem com setup simplificado.

---

## Links Úteis
*   **Repositório Oficial (GitHub):** [https://github.com/All-Hands-AI/OpenHands](https://github.com/All-Hands-AI/OpenHands)
*   **Site Oficial:** [https://www.all-hands.dev/](https://www.all-hands.dev/)
*   **OpenHands Cloud:** [https://openhands.dev/](https://openhands.dev/)
