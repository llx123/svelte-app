<script>
  export let name;

  import TodoHeader from "./TodoHeader.svelte";
  import TodoList from "./TodoList.svelte";
  import { itemStore } from "./store";
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <div>Total item: {$itemStore.length}</div>
  <TodoHeader />
  <TodoList />

  <h1>Hello {name}!</h1>
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
  <p>https://iiong.com/sveltejs-study-notes/</p>
  <p>https://svelte.dev/</p>
</main>
