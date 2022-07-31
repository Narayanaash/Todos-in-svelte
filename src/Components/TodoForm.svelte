<script>
</script>

<form>
  <div class="todo__inputBox">
    <input
      class="todo__inputBox__input"
      type="search"
      placeholder="Type here something..."
      autofocus
    />
    <button class="todo__inputBox__btn" type="submit">Submit</button>
  </div>
</form>

<style>
  .todo__inputBox {
    background-color: white;
    border: 2px solid white;
    border-radius: 6px;
    height: 46px;
    display: flex;
    align-items: center;
  }
  .todo__inputBox__input {
    background: no-repeat;
    border: 0;
    width: calc(100% - 100px);
    height: 100%;
    font-size: 16px;
    font-weight: 600;
    padding: 5px 12px;
    color: inherit;
  }
  .todo__inputBox__btn {
    width: 98px;
    height: calc(100% - 4px);
    font-weight: bold;
    cursor: pointer;
    border-radius: 6px;
    background: #0075ff;
    color: white;
    font-size: 16px;
  }
  .todo__inputBox__btn:hover {
    background: linear-gradient(-45deg, #7d27b0cc, #ff00008a);
    color: white;
  }
</style>
