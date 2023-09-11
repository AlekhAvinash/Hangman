<script>
  export let key = "";
  export let ele
  let visible = true;
  function toggleVissible() {
    visible = !visible
    ele.update(key)
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