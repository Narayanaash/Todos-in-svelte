<script>
  import TodoItem from "./TodoItem.svelte";

  export let todos = [];
  export let removeFromTodos;
</script>

<ul class="todo__list">
  {#each todos as todo (todo.id)}
    <TodoItem {todo} on:remove={removeFromTodos} />
  {/each}
</ul>

<style>
  .todo__list {
    padding-top: 6px;
  }
</style>
