<script>
	const num = -3
</script>

<main>
	{#if num==0}
		<h2>The number is zero</h2>
	{:else if num<0}
		 <h2>Num is negetive</h2>
	{:else if num>0}
		 <h2>Num is positive</h2>
	{:else }
	<h2>The number is not</h2>
	{/if}

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