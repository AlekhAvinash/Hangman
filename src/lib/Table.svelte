<script lang="ts">
  import Cell from "./Cell.svelte"
  export let ele
</script>

<div id="keyboard">
  <div class="kb-row">
    <Cell key="q" ele = {ele}/>
    <Cell key="w" ele = {ele}/>
    <Cell key="e" ele = {ele}/>
    <Cell key="r" ele = {ele}/>
    <Cell key="t" ele = {ele}/>
    <Cell key="y" ele = {ele}/>
    <Cell key="u" ele = {ele}/>
    <Cell key="i" ele = {ele}/>
    <Cell key="o" ele = {ele}/>
    <Cell key="p" ele = {ele}/>
  </div>
  <div class="kb-row">
    <Cell key="a" ele = {ele}/>
    <Cell key="s" ele = {ele}/>
    <Cell key="d" ele = {ele}/>
    <Cell key="f" ele = {ele}/>
    <Cell key="g" ele = {ele}/>
    <Cell key="h" ele = {ele}/>
    <Cell key="j" ele = {ele}/>
    <Cell key="k" ele = {ele}/>
    <Cell key="l" ele = {ele}/>
  </div>
    <div class="kb-row">
    <Cell key="z" ele = {ele}/>
    <Cell key="x" ele = {ele}/>
    <Cell key="c" ele = {ele}/>
    <Cell key="v" ele = {ele}/>
    <Cell key="b" ele = {ele}/>
    <Cell key="n" ele = {ele}/>
    <Cell key="m" ele = {ele}/>
  </div>
</div>

<style>
  #keyboard {
    margin: 5px;
  }

  .kb-row {
    display: flex;
    width: 100%;
    justify-content: center!important;
    margin: 10px 0;
  }
</style>