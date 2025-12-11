

<script>
import Footer from "$lib/components/Footer.svelte"
  let books = $state([
    { id: 1, name: "HTML for Hamsters" },
    { id: 2, name: "CSS: Cannot Style Sandwiches" },
    { id: 3, name: "JavaScript and the Fifty Shades of Errors" },
  ]);

  const removeBook = (id) => {
    books = books.filter((book) => book.id != id);
  };
</script>

<h1>Books</h1>

<ul>
  {#each books as book}
    <li>
      {book.name}
      <button onclick={() => removeBook(book.id)}>Remove</button>
    </li>
  {/each}
</ul>

<footer />


