<script>

  export let style = undefined;
  export let disabled = false;
  export let classes = undefined;
  export let id = undefined;

</script>

<button type="button" on:click {disabled} {id} {style} class={classes}><slot/></button>

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
    background-color: transparent;
  }

  button:hover {
    background: none;
    cursor: pointer;
  }
  button:focus,
  button:focus-visible {
    outline: none;
  }

</style>