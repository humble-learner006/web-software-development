<script>
    let todos = $state([
        { id: 0, text: "Sample todo", done: false },
    ]);
    let todoName = $state(""); // 用于输入待办事项文本
    let nextId = $state(1); // 维护一个单独的ID计数器，避免依赖数组长度

    const addTodo = () => {
        if (todoName.trim() === "") return;

        const todo = {
            id: nextId++,
            text: todoName.trim(), // 使用 text
            done: false, // 明确设置 done 状态
        };

        todos.push(todo);
        todoName = ""; // 清空输入框
    };

    const changeToComplete = (id) => {
        // 使用 find 找到点击的 todo
        const selectedTodo = todos.find(t => t.id === id); 
        
        if (selectedTodo) {
            // 直接修改找到的对象（Svelte $state 允许这种做法）
            selectedTodo.done = true; 
        }
    };
</script>

<!-------line here -------->

<h1>Todos</h1>

<input type="text" bind:value={todoName} placeholder="Add new todo here" />
<button onclick={addTodo}>Add</button>

<h2>Pending</h2>
<ul>
  {#each todos.filter(t => !t.done) as todo (todo.id)}
    <li>
      {todo.text}
      <button onclick={() => changeToComplete(todo.id)}>Mark as done</button>
    </li>
  {/each}
</ul>

<h2>Completed</h2>
<ul>
  {#each todos.filter(t => t.done) as todo (todo.id)}
    <li>
      <!-- <span style="text-decoration: line-through;">{todo.text}</span> -->
      {todo.text}
    </li>
  {/each}
</ul>
