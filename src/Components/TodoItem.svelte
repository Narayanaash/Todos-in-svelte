<script>
  import Close from "./ui/Close.svelte";

  export let todo = {};
</script>

<li class="todo__item">
  <label>
    <input type="checkbox" />
    <span>{todo.title}</span>
  </label>
  <Close />
</li>

<style>
  .todo__item {
    list-style: none;
    background-color: white;
    border-radius: 6px;
    margin-top: 6px;
    font-weight: 600;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 8px;
  }
  .todo__item label {
    padding: 14px 13px;
    display: flex;
    align-items: center;
    line-height: 1;
    flex-grow: 1;
  }
  .todo__item:hover {
    background-color: rgb(241, 241, 241);
  }
  .todo__item input {
    cursor: pointer;
    width: 18px;
    height: 18px;
    margin-right: 10px;
  }
  .todo__item input:checked ~ span {
    text-decoration: line-through;
  }
</style>
