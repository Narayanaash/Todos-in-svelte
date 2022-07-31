<script>
  import TodoForm from "./Components/TodoForm.svelte";
  import TodoList from "./Components/TodoList.svelte";

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
</script>

<main>
  <div class="todo">
    <div class="todo__box">
      <TodoForm />
      <TodoList todoList={todos} />
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
