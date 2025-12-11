<h1>books!</h1>
<p><a href="/books/1">Go to page book 1</a></p>

<h2>Description</h2>
<p>This route is design for practicing dynamic update the content</p>

In +page.svelte, the data property read via $props() comes from the page’s load() function. Regular child components do not get that data automatically: instead, you must pass properties to them explicitly.

