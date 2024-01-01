<script>
  import { onMount } from 'svelte';

  let message = 'Loading...';

  onMount(async () => {
    const response = await fetch('http://localhost:8400');
    const data = await response.json();
    message = data.Hello;
  });
</script>

<main>
  <h1>Hello {message}!</h1>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  h1 {
    color: #ff3e00;
    font-size: 2em;
  }
</style>
