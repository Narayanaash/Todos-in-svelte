<script>
  import TodoItem from "./TodoItem.svelte";

  export let todoList = [];
</script>

<ul class="todo__list">
  {#each todoList as todo (todo.id)}
    <TodoItem {todo} />
  {/each}
</ul>

<style>
  .todo__list {
    padding-top: 6px;
  }
</style>
