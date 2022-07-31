<script>
  import { onMount } from "svelte";
  import TodoForm from "./components/TodoForm.svelte";
  import TodoList from "./components/TodoList.svelte";

  let ref;

  onMount(() => {
    ref.focus();
  });

  let todos = [
    {
      title: "Todo list item 1",
      id: 1,
      isDone: false,
    },
    {
      title: "Todo list item 2",
      id: 2,
      isDone: true,
    },
    {
      title: "Todo list item 3",
      id: 3,
      isDone: false,
    },
    {
      title: "Todo list item 4",
      id: 4,
      isDone: false,
    },
  ];

  let newTodo;

  function addToList() {
    if (!newTodo) {
      return;
    }
    todos = [{ title: newTodo, id: Math.random(), isDone: false }, ...todos];
    newTodo = "";
  }

  function removeFromTodos(event) {
    todos = todos.filter((todo) => todo.id !== event.detail.id);
    todos = todos;
  }
</script>

<main>
  <div class="todo">
    <div class="todo__box">
      <TodoForm bind:newTodo {addToList} bind:ref />
      <TodoList {todos} on:remove={removeFromTodos} {removeFromTodos} />
    </div>
  </div>
</main>

<style>
  .todo {
    width: 100vw;
    min-height: 100vh;
    display: grid;
    place-items: center;
    background-image: linear-gradient(45deg, #7d27b0cc, #ff00008a);
  }
  .todo__box {
    width: 100%;
    max-width: 500px;
    margin-top: 30px;
  }
</style>
