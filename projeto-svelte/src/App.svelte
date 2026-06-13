<script>
  import Component from './Component.svelte';

  let participantes = $state(['Emilly', 'João Pedro', 'Pedro Daniel', 'Ray']);
  let novoNome = $state('');
  let sorteado = $state('');

  let quantidade = $derived(participantes.length);

  function adicionarParticipante() {
    const nome = novoNome.trim();
    if (nome === '') {
      return;
    }
    participantes.push(nome);
    novoNome = ''; 
  }

  function removerParticipante(i) {
    participantes.splice(i, 1);
    sorteado = ''; 
  }

  function sortear() {
    if (participantes.length === 0) {
      return;
    }
    const i = Math.floor(Math.random() * participantes.length);
    sorteado = participantes[i];
  }

  function evEnter(evento) {
    if (evento.key === 'Enter') {
      adicionarParticipante();
    }
  }
</script>

<main>
  <h1>Sorteador de Nomes</h1>

  <div class="digite-nome">
    <input
      type="text"
      placeholder="Digite um nome"
      bind:value={novoNome}
      onkeydown={evEnter}
    />
    <button onclick={adicionarParticipante}>Adicionar</button>
  </div>

  <p class="contagem">Participantes: {quantidade}</p>

  {#if participantes.length === 0}
    <p class="vazio">Nenhum participante</p>
  {:else}
    <ul>
      {#each participantes as nome, i}
        <Component nome={nome} i={i} momentoRemover={removerParticipante} />
      {/each}
    </ul>
    <button class="sortear" onclick={sortear}>Sortear</button>
  {/if}

  {#if sorteado !== ''}
    <p class="resultado">O sorteado foi: <strong>{sorteado}</strong></p>
  {/if}
</main>

<style>
  main {
    max-width: 480px; margin: 2rem auto; padding: 1.5rem;
    background: white; border-radius: 8px;
		border: 2px solid black;
  }
  h1 { text-align: center; color: darkorange; }
  .digite-nome { display: flex; gap: 0.5rem; margin-bottom: 1rem; }
  .digite-nome input { flex: 1; padding: 0.5rem; font-size: 1rem; }
  .digite-nome button {
    padding: 0.5rem 1rem; background: #ff3e00; color: white;
    border: none; border-radius: 4px; cursor: pointer;
  }
  .contagem { text-align: center; color: black; }
  .vazio { text-align: center; color: black; font-style: italic; }
  ul { list-style: none; padding: 0; color: black }
  .sortear {
    display: block; width: 100%; padding: 0.8rem; margin-top: 1rem;
    font-size: 1.1rem; background: #2c3e50; color: white;
    border: none; border-radius: 4px; cursor: pointer;
  }
  .resultado {
    text-align: center; font-size: 1.3rem; margin-top: 1.5rem; color: #2c3e50;
  }
</style>
