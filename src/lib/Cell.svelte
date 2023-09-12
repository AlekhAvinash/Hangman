<script>
  export let key = "";
  export let ele
  let visible = true;
  let out = true
  function toggleVissible() {
    visible = !visible
    out = ele.update(key)
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
    class="btn btn-outline-{out? 'success' : 'danger'} disabled"
  >
    {key.toUpperCase()}
  </tr>
{/if}