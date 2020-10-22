<script lang="typescript">
  import './tw.css';

  import {onMount} from 'svelte';
  let count: number = 0;

  onMount(() => {
    const interval = setInterval(() => count++, 1000);
    return () => {
      clearInterval(interval);
    };
  });
</script>

<style>
  :global(body) {
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
  }
</style>

<div class="text-center">
  <header class="flex flex-col justify-center h-screen w-full">
    <img src="/logo.svg" class="h-64 m-3" alt="logo" />
    <p>Edit <code>src/App.svelte</code> and save to reload.</p>
    <p class="bg-gray-200">Page has been open for <code class="bg-gray-600 text-white">{count}</code> seconds.</p>
    <p>
      <a class="" href="https://svelte.dev" target="_blank" rel="noopener noreferrer">
        Learn Svelte
      </a>
    </p>
  </header>
</div>
