<script>
  let { data } = $props();
</script>

<h1>Todo {data.todoId}, task {data.taskId}</h1>

<a href="/todos/{data.todoId}">Back to todo</a>