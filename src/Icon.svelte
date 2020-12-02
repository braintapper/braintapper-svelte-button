<script>

  export let style = undefined;
  export let disabled = false;
  export let classes = undefined;
  export let id = id;

</script>

<button type="button" on:click {style} {disabled} class={classes}><slot></slot></button>

<style>

  button {
    display: inline-block;
    padding: 0px;
    background: none;
    height: 24px;
    min-width: 24px;
    width: 24px;
    border: none;
    margin: 0px;
  }

  button:hover {
    background: none;
    cursor: pointer;
  }
</style>