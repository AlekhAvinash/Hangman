<script lang="ts">
  import Table from "./lib/Table.svelte"
  import Word from "./lib/Word.svelte"
  let word
</script>

<main>
  <Word bind:this={word}/>
  <Table ele={word}/>
</main>

<style>
main {
  background-color: var(--bs-dark);
}
</style>