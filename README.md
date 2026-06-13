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
- npm create vite@latest projeto-svelte -- --template svelte
- cd projeto-svelte
- npm install
- npm run dev

**Passo-a-Passo para o desenvolvimento**  

Iniciei o processo pesquisando sobre o Svelte de forma geral. A maior parte dos materiais e estudos que encontrei era referente a versões 
anteriores do Svelte 5, então recorri diretamente ao site oficial svelte.dev, onde li toda a documentação e acompanhei o tutorial 
disponível. No YouTube, os vídeos encontrados também abordavam versões antigas ou projetos mais complexos com o SvelteKit.  
![Documentação Svelte](https://github.com/PedroD18/Seminario-mini-projeto/blob/35bb4a873e310adb73942fdefede072b097af154/Documenta%C3%A7%C3%A3o.png) 
![Tutorial Svelte](https://github.com/PedroD18/Seminario-mini-projeto/blob/cca00426a02d5f716132d91e273a959fac1c34a7/Tutorial.png)

Para dar início ao mini projeto, utilizei o Svelte Online Playground, disponível no próprio svelte.dev. Por se tratar de um ambiente 
simples sem necessidade de instalação consegui desenvolver e concluir o projeto. O tema escolhido foi um sorteio de
pessoas que se mostrou ideal para demonstrar os conceitos do Svelte de forma clara e objetiva.  
![Svelte Playground](https://github.com/PedroD18/Seminario-mini-projeto/blob/ef98a345944a37d61023928e0fd0cfe47a88ac24/Svelte%20Playground.png)

Em seguida pesquisei no ChatGPT e no Gemini como configurar as dependências no GitHub Codespaces. Ambos recomendaram o uso do Vite, uma 
ferramenta de build mais simples e adequada para projetos como o meu que envolvia apenas o Front-End. Utilizei IA também para identificar
e corrigir um erro que estava ocorrendo na porta do Vite, além de ajustar o CSS padrão que vinha configurado por padrão na ferramenta.

![Projeto Codespace]()  


![Projeto Pronto]()





