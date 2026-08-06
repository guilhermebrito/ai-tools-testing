# OpenHands

## Visão Geral
OpenHands (anteriormente denominado OpenDevin) é uma iniciativa open-source muito ativa focada na construção de um Engenheiro de Software de IA completamente autônomo. Ele substitui a intervenção humana atuando como um desenvolvedor individual, englobando a descoberta, o planejamento, e o conserto ponta-a-ponta de grandes trechos de software.

## Principais Funcionalidades / Como Funciona
- **Autonomia Completa do Ciclo de Software:** O agente busca problemas ou aceita pedidos via interface, constrói planos formais, roda *scripts* de validação em terminal e reinicia processos após falhas (auto-cura).
- **Abordagem de Contêiner Seguro (Sandboxing):** Opera as alterações em um repositório isolado via Docker, podendo quebrar dependências do sistema global temporário sem impacto à máquina base do desenvolvedor ou prod.
- **Navegador Embutido:** Suporta visualização da Internet para leitura contínua de documentações de *frameworks* novos ou iteração visual (teste de botões e links de UI).

## Pontos Fortes e Limitações
### Pontos Fortes
- **Segurança de Execução Total:** Executar códigos ou *libraries* maliciosas (hallucinated packages) geradas por IA fica irrelevante pelo robusto isolamento de contêineres Docker.
- **Suporte Nativo Imenso:** Roteia *prompts* entre dezenas de provedores de API, permitindo comparar resultados localmente ou pela nuvem facilmente.

### Limitações
- O loop de "tentativa-e-erro" (quando o agente erra o build muitas vezes) pode drenar o orçamento via consumo altíssimo de Tokens.
- *Workspace* mapeados e uso de contêineres podem consumir recursos vastos da memória e CPU local.

## Casos de Uso
- Integração profunda com provedores Git (GitHub/GitLab) para fechar *Issues* autônomas durante os *sprints*.
- Extração lógica, documentação autogerada e refatoração agressiva de legados com garantia isolada.
- Prototipagem ultra-rápida e scripts ponta a ponta independentes.

## Status, Preço e Licenciamento
- **Modelo:** Open-Source (Licença MIT).
- **Preço:** Gratuito; porém necessita uso intensivo de LLMs pagos externos.
- **Agnóstico de Provedor:** Sim.

## Links Úteis
- **Repositório Oficial (GitHub):** [https://github.com/All-Hands-AI/OpenHands](https://github.com/All-Hands-AI/OpenHands)
- **Site Oficial:** [https://www.all-hands.dev/](https://www.all-hands.dev/)
