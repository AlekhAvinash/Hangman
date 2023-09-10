<script lang="ts">
  import Cell from "./Cell.svelte"
</script>

<div id="keyboard">
  <div class="kb-row">
    <Cell key="q"/>
    <Cell key="w"/>
    <Cell key="e"/>
    <Cell key="r"/>
    <Cell key="t"/>
    <Cell key="y"/>
    <Cell key="u"/>
    <Cell key="i"/>
    <Cell key="o"/>
    <Cell key="p"/>
  </div>
  <div class="kb-row">
    <Cell key="a"/>
    <Cell key="s"/>
    <Cell key="d"/>
    <Cell key="f"/>
    <Cell key="g"/>
    <Cell key="h"/>
    <Cell key="j"/>
    <Cell key="k"/>
    <Cell key="l"/>
  </div>
    <div class="kb-row">
    <Cell key="z"/>
    <Cell key="x"/>
    <Cell key="c"/>
    <Cell key="v"/>
    <Cell key="b"/>
    <Cell key="n"/>
    <Cell key="m"/>
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