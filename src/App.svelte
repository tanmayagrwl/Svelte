<script>
	const name = 'Batman'
	const channel = '<b>codevolution</b>'
	const headingId = 'heading'
	const disabled = true
	const status = 'success'
	const isPromoted = true
</script>

<main>
	<h2 class="underline">Underlined text</h2>
	<h2 class={status}>status</h2>
	<h2 class={isPromoted ? 'promoted' : 'danger'}>Movie title</h2>
	<h1>Hello {name}</h1>
	<div>{@html channel}</div>
	<h2 id={headingId}>This is a heading</h2>
	<button {disabled}>Bind</button>
</main>

<style>
	.underline{
		text-decoration:underline ;
	}

	.danger{
		color: red;
	}

	.success{
		color: olive;
	}

	.promoted{
		font-style: italic;

	}

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>