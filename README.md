# Seminario-mini-projeto

**Descrição do objetivo**  

O objetivo deste projeto é demonstrar na prática os principais recursos do Svelte: 
- Reatividade (state e derived).
- Os componentes e comunicação entre componentes (props e callbacks).
- A ligação de dados de mão dupla (bind:value), e renderização condicional e de listas ({#if} e {#each}).
  
O projeto permite ao usuário:
- Adicionar nomes a uma lista de participantes;
- Remover participantes;
- Sortear aleatoriamente um nome da lista;
- Ver a contagem de participantes atualizada automaticamente.

**Descrição para instalação dos softwares necessários** 

Foi Utilizado o gitHub codespaces não é preciso instalar nada na sua máquina. Tudo roda no navegador em um ambiente na nuvem que já vem com node, npm e git instalados.    
- Svelte 5
- Vite: Ferramenta de build que cria, compila e serve o projeto durante o desenvolvimento. (OBS: O Svelte é um compilador, então os arquivos .svelte precisam ser transformados em javaScript antes de rodar no navegador. O Vite é a ferramenta oficialmente recomendada para isso hoje.)
- Node.js
  
No terminal do Codespaces:
- npm create vite@latest meu-app -- --template svelte
- cd projeto-svelte
- npm install



