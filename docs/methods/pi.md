# Pi (earendil-works/pi/coding-agent)

## Visão Geral
O Toolkit Pi (com ênfase no seu módulo `coding-agent`) atua como uma solução open-source e robusta de fundação, focada em empoderar desenvolvedores a montar, customizar e implantar seus próprios bots ou interfaces CLI conversacionais voltadas para uso corporativo interno e desenvolvimento pesado.

## Principais Funcionalidades / Como Funciona
- **Interface Rica no Terminal (TUI):** Traz uma experiência quase gráfica para dentro da CLI bruta. É capaz de desenhar menus selecionáveis visualmente atraentes e barras interativas utilizando os recursos modernos do emulador de terminal.
- **API Unificada de IA:** Abstrai fortemente os percalços ao trocar os conectores LLM da OpenAI, Google ou hospedeiros locais como vLLM. O código do seu Agente se mantém igual independentemente do cérebro acoplado.
- **Integração de Bots Externos (ChatOps):** Oferece utilitários de suporte de primeira classe para Slack e Discord bots, conectando os LLMs locais aos canais da equipe de forma contínua.

## Pontos Fortes e Limitações
### Pontos Fortes
- **Aceleração para Builders (Hackability):** Extremamente maleável. Se você não gosta do Cursor e quer fazer sua própria plataforma central de Inteligência Artificial usando sua cloud fechada, este toolkit diminui o atrito sensivelmente.
- **Conectividade de Ecossistemas Híbridos:** É otimizado para lidar muito bem com contêineres locais rodando Modelos Menores ou *LLMs Open-Weights* corporativas fechadas em LGPD.

### Limitações
- Não é um "Assistente AI" de prateleira para meramente baixar e começar a codar magicamente no seu código pessoal como as IDEs da moda. Requer visão arquitetural de implantação.

## Casos de Uso
- Criação e montagem do chat de suporte e revisão de código proprietário no servidor "on-premise" interno do seu cliente (via conexões isoladas e modelos locais privados).
- Implantação rápida de um Bot central no Slack da Engenharia respondendo *Queries* lendo do repositório *core*.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source.
- **Preço:** Totalmente gratuito.
- **Agnóstico de Provedor:** Sim.

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/earendil-works/pi](https://github.com/earendil-works/pi)
