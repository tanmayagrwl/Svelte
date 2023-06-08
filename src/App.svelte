<script>
	const names= ['bruce', 'clark', 'diana']
	const age= ['11', '12', '13']
	const deets = [
		{first : 'abc', age: 11},
		{first : 'ssd', age: 121},
		{first : 'sd', age: 121},
	]
</script>

<main>
	{#each deets as deet,index}
	<h1>{index+1} {deet.first} {deet.age}</h1>
	{/each}
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