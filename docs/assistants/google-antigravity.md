# Google Antigravity

## Visão Geral
Google Antigravity é um assistente de codificação e engenharia de software *agentic* altamente avançado, desenvolvido pela equipe do Google DeepMind. Mais do que um autocompletar, ele atua ativamente como um desenvolvedor parceiro integrado ao ambiente do usuário.

## Principais Funcionalidades / Como Funciona
- **Planning Mode:** Capaz de gerar, documentar e iterar sobre planos de arquitetura rígidos antes de executar modificações no código.
- **Execução Sandboxed:** Executa ferramentas e comandos no terminal de forma segura, com opções de restrição de rede e disco (*sandbox*).
- **Agentic Workflow (Subagentes):** Orquestra múltiplos agentes simultaneamente para diferentes tarefas (ex: sub-agente de pesquisa no código, sub-agente de navegação na web).
- **Consciência de Estado Profunda:** Monitora ativamente o contexto do editor atual do usuário (abas ativas, posição do cursor, seleções textuais).

## Pontos Fortes e Limitações
### Pontos Fortes
- **Autonomia "End-to-End":** Recebe tarefas de alto nível, formula o plano lógico, altera arquivos, e depura os próprios erros com extrema resiliência.
- **Orquestração de Navegação Web:** A capacidade de instanciar um *browser* internamente o torna ímpar para desenvolver e testar aplicações de interface gráfica autonomamente.

### Limitações
- Sua total eficiência é demonstrada em tarefas grandes, podendo ser "exagerado" (overkill) para alterações minúsculas pontuais.
- Atrelado tecnologicamente ao ecossistema e modelos do Google.

## Casos de Uso
- Construção de novas funcionalidades inteiras de software do zero, guiadas pelo *Planning Mode*.
- Depuração interativa e resolução autônoma de *bugs* que quebram o processo de compilação/build.
- Integração de testes ponta-a-ponta (E2E) em sistemas web complexos.

## Status, Preço e Licenciamento
- **Modelo:** Proprietário.
- **Preço:** Sujeito à plataforma e política comercial da infraestrutura Google Gemini.
- **Agnóstico de Provedor:** Não (Alimentado por modelos do Google).

## Links Úteis
- **Site Oficial:** [https://deepmind.google/](https://deepmind.google/)
