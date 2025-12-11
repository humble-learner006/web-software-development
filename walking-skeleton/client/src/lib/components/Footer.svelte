<script>
 let tests = [
    { path: "/test/test1", name: "Text transformations" },
    { path: "/test/test2", name: "Books with remove buttons" },
    { path: "/test/test3", name: "Books with add buttons" },
    { path: "/books", name: "Books with dynamic update function" },
    { path: "/todos", name: "Double layer, todo and task structure" }
  ];
</script>

<footer>
  <h1>---- This is Footer part ----</h1>
  <p>Thanks for visiting!</p>
  <h2>Basic Page Navigation</h2>
  <nav>
    <ul>
      <li><a href = "/">Home page</a></li>
      <li><a href = "/contact">Contact page</a></li>
      <li><a href = "/about">About page</a></li>
    </ul>
  <h2>Practice sample code</h2>
    <nav>
    <ol>
      {#each tests as test}
        <li>
          <a href={test.path}>{test.name}</a>
        </li>
      {/each}
    </ol>
</footer>