<script>
    let text = $state("why it can pass through")
    const textChanged = (event) => {
        text = event.target.value;
    }
</script>
<input type="text" oninput={textChanged} />
<p>Text: {text} </p> 
<p>Length: {text.length}</p>
<p>Lowercase: {text.toLowerCase()}</p>
<p>Uppercase: {text.toUpperCase()}</p>
