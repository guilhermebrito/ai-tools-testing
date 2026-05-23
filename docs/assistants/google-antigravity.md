# Google Antigravity

## Visão Geral
Google Antigravity é um assistente de codificação agentic (autônomo) avançado, desenvolvido pela equipe do Google DeepMind. Mais do que um simples autocompletar, ele opera como um "Engenheiro de Software Júnior/Pleno" trabalhando ao seu lado.

## Como Funciona
Antigravity possui acesso profundo e seguro ao ambiente de trabalho do usuário. Ele pode:
- Usar ferramentas de busca e visualização de arquivos de forma independente.
- Planejar arquiteturas antes de escrever o código (Planning Mode).
- Executar comandos no terminal (compilar, rodar testes, subir servidores locais).
- Iniciar um "Browser Subagent" para navegar na web, ler documentações ou testar visualmente a UI que acabou de codificar.

## Pontos Fortes
- **Autonomia "End-to-End":** É capaz de receber uma tarefa macro ("Crie um formulário de login com autenticação Clerk") e realizar todas as micro-tarefas necessárias (instalar libs, escrever o código, testar e debugar erros de build).
- **Consciência de Estado:** Entende o que o desenvolvedor está fazendo no momento (quais arquivos estão abertos, onde está o cursor).

## Casos de Uso
- Desenvolvimento de features completas de ponta a ponta.
- Resolução autônoma de bugs em que a causa não é imediatamente óbvia.
- Testes end-to-end integrando terminal, código e navegador.

## Links Úteis
- **Site Oficial:** [https://deepmind.google/](https://deepmind.google/)
