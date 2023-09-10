<script>
  export let key = "";
  let visible = true;
  function toggleVissible() {
    visible = !visible
  }
</script>

{#if visible}
  <button 
    on:click={toggleVissible}
    class="btn btn-outline-primary"
  >
    {key.toUpperCase()}
  </button>
{:else}
  <tr
    class="btn btn-outline-success disabled"
  >
    {key.toUpperCase()}
  </tr>
{/if}