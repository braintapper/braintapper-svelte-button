<script>

  export let disabled = undefined;
  export let state = "primary";
  export let style = undefined;
  export let classes = undefined;
  export let id = undefined;

  
</script>

<button type="button" {disabled} {id} {state} {style} class={classes} on:click><slot/></button>

<style>

  button {
    font-family: var(--font-family-primary), -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    width: auto;
    padding: 6px 12px;
    background-color: var(--lighter-gray);
    color: var(--black);
    border-radius: 4px;
    border: none    
  }

  button:hover {
    background-color: var(--lightest-gray);
    cursor: pointer;
  }

  button:active,
  button:focus {
    background-color: var(--gray);
  }

  button[disabled],
  button[disabled]:hover,
  button[disabled]:focus,
  button[disabled]:active {
    background: var(--lightest-gray);
    color: var(--light-gray);
  }

  
  button[state="critical"] {
    background-color: var(--critical);
    color: var(--white);
  }

  
  button[state="critical"]:hover {
    background-color: var(--critical-hover);
  }


  button[state="critical"]:active,
  button[state="critical"]:focus {
    background-color: var(--critical-active);
  }


  button[state="critical"][disabled],
  button[state="critical"][disabled]:hover,
  button[state="critical"][disabled]:focus,
  button[state="critical"][disabled]:active {
    background-color: var(--critical-disabled);
    color: var(--dark-gray);
  }


  button[state="primary"] {
    background-color: var(--primary);
    color: var(--white);
  }

  
  button[state="primary"]:hover {
    background-color: var(--primary-hover);
  }


  button[state="primary"]:active,
  button[state="primary"]:focus {
    background-color: var(--primary-active);
  }


  button[state="primary"][disabled],
  button[state="primary"][disabled]:hover,
  button[state="primary"][disabled]:focus,
  button[state="primary"][disabled]:active {
    background-color: var(--primary-disabled);
    color: var(--dark-gray);
  }

</style>