# Hermes (Nous Research)

## Visão Geral
Hermes é um agente de Inteligência Artificial open-source concebido pela Nous Research. Seu diferencial marcante é a sua atuação como um assistente pessoal altamente customizável e persistente, projetado especialmente para automatizar fluxos de trabalho locais de desenvolvedores de software e operadores de infraestrutura.

## Principais Funcionalidades / Como Funciona
- **Sistema de "Skills" (Auto-aperfeiçoamento):** O Hermes pode abstrair fluxos de sucesso que ele executa, convertendo-os e salvando-os em novos documentos Markdown ("Skills"). No futuro, ele aplica essas Skills para tarefas similares de forma automatizada e barata.
- **Orquestrador CLI:** Opera nativamente no terminal e orquestra execuções de sistema, cria e manipula arquivos locais e dispara scripts Python.
- **Integrações Multicanal:** Suporta conexões de entrada de dados (Gateways) para Telegram, Slack, E-mail e Discord, permitindo, por exemplo, o envio de um comando por voz no Telegram.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Privacidade Excepcional e Self-Hosting:** Pode rodar em redes isoladas sem vazamento de código fonte corporativo.
- **Capacidade Evolutiva:** Devido à biblioteca de *Skills*, o agente ganha "experiência de projeto" progressivamente, não começando do zero a cada execução.

### Limitações
- Configuração inicial e arquitetura possuem viés altamente técnico (não *plug-and-play*).
- Menos adaptado a gerar interfaces *front-end* e layouts comparado ao *Cursor* ou *Google Antigravity*.

## Casos de Uso
- Operação permanente em VPS privadas ou *home-servers* para administração remota (DevOps).
- Delegação de tarefas demoradas via chat de celular (ex: acionar um *redeploy* de infraestrutura longa no trânsito).
- Automação de pipelines pesados de CI/CD não enquadrados nas limitações do GitHub Actions convencionais.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source.
- **Preço:** Gratuito (O usuário fornece sua própria infraestrutura e chaves de API/Ollama).
- **Agnóstico de Provedor:** Sim.

## Links Úteis
- **Nous Research:** [https://nousresearch.com/](https://nousresearch.com/)
- **Repositório Oficial (GitHub):** [https://github.com/NousResearch/Hermes](https://github.com/NousResearch/Hermes)
