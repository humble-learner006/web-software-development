<!-- <script>
  let { data } = $props();
</script>

<p>Todo {data.todoId}</p> -->




<!-- <script>
  let { data } = $props();

  let todoId = $derived(parseInt(data.todoId));
  let nexttodoId = $derived(todoId + 1);
</script>

<h1>Todo {todoId}</h1>

<a href="/todos/{nexttodoId}">Go to next todo</a> -->




<!-- 我他妈服了！上次是Id 和 ID 大小写出错，这次是没加上中括号 -->

<script>
  let { data } = $props();

  let todoId = $derived(parseInt(data.todoId));
  let nexttodoId = $derived(todoId + 1);
</script>

<h1>Todo {todoId}</h1>

<p><a href="/todos/{todoId}/tasks/1">Go to first task</a></p>
<p><a href="/todos/{nexttodoId}">Go to next todo</a></p>
<p><a href="/todos">Back to Todo</a></p>
<p><a href="/">Back to Homepage</a></p>
