<script>
  let { nome, i, momentoRemover } = $props();
</script>

<li>
  <span>{nome}</span>
  <button class="remover" onclick={function () { momentoRemover(i); }}>
    Remover
  </button>
</li>

<style>
  li {
    display: flex; justify-content: space-between; align-items: center;
    padding: 0.5rem; border-bottom: 1px solid #ddd;
  }
  .remover {
    background: #e74c3c; color: white; border: none;
    padding: 0.3rem 0.6rem; border-radius: 4px; cursor: pointer;
  }
</style>