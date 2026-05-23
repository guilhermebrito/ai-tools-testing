# OpenHands

## Visão Geral
OpenHands (anteriormente conhecido como OpenDevin) é uma plataforma open-source desenvolvida para atuar como um Engenheiro de Software de Inteligência Artificial autônomo. Ele atua como um agente independente capaz de realizar tarefas complexas de desenvolvimento de software end-to-end.

## Funcionalidades Principais
- **Autonomia de Execução:** Capaz de explorar o repositório, planejar a solução, escrever código, rodar testes no terminal e iterar iterativamente até que a tarefa seja concluída.
- **Ambiente Seguro (Sandboxed):** Utiliza containers Docker para criar um ambiente de trabalho seguro e isolado, onde o agente pode rodar comandos CLI e compilar código sem risco ao sistema operacional principal.
- **Navegação Web:** Possui a capacidade de abrir um navegador web virtualmente para pesquisar e ler documentações na internet ou testar visualmente aplicações web construídas.
- **Suporte Multi-Modelo:** Totalmente agnóstico a LLMs, suportando provedores grandes como OpenAI, Anthropic, Google, além de OpenRouter e LLMs rodando localmente via Ollama.

## Casos de Uso
- Resolução de *Issues* e correção de *bugs* de forma autônoma.
- Criação de aplicações, scripts e automações end-to-end.
- Exploração, documentação e refatoração de grandes bases de código legado.

## Status
- **Open Source:** Sim (Licença MIT).
- **Gratuito:** Sim (O software é gratuito, mas requer que o usuário forneça sua própria chave de API de LLMs ou utilize modelos locais).

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/All-Hands-AI/OpenHands](https://github.com/All-Hands-AI/OpenHands)
- **Site Oficial:** [https://www.all-hands.dev/](https://www.all-hands.dev/)
