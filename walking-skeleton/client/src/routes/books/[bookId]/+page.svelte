<!-- <script>
  let { data } = $props();
</script>

<p>book {data.bookId}</p> -->

<script>
  let { data } = $props();

  let bookId = $derived(parseInt(data.bookId));
  let nextBookId = $derived(bookId + 1);
</script>

<p>book {data.bookId}</p>

<p>Current book id: {bookId}</p>
<p>Next book id: {nextBookId}</p>

<p><a href="/books/{nextBookId}">Next book</a></p>


<!-- 我真的服了，一直没找出来的问题原来是路径名称是 bookId 而非我错误打字的 bookID 
还有一个问题是 +page.js wrongly typed as page.js 
-->