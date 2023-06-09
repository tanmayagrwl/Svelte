<script>
	const formValues = {
		name : '',
		profileSummary: '',
		country:'',
		jobLocation : [],
	}

</script>

<main>
	<div>
		<pre>
			{JSON.stringify(formValues,null,2)}
		</pre>
	</div>
	<form >
		<div>
			<label for="name">Name</label>
			<input type="text" id="name" bind:value={formValues.name}/>
		</div>
		<div>
			<label for="profileSummary">Profile Summary</label>
			<textarea id="profileSummary" bind:value={formValues.profileSummary}></textarea>
		</div>
		<div>
			<label for="country">Country</label>
			<select name="counrty" id="counrty" bind:value={formValues.country}>
				<option value="">Select a country</option>
				<option value="India">India</option>
				<option value="Vietnam">Vietnam</option>
				<option value="Singapore">Singapore</option>	
			</select>
		</div>
		<div>
			<label for="job-Location">Job location</label>
			<select name="job-location" id="job-location" bind:value={formValues.jobLocation} multiple>
				<option value="">Select a country</option>
				<option value="India">India</option>
				<option value="Vietnam">Vietnam</option>
				<option value="Singapore">Singapore</option>	
			</select>
		</div>
	</form>
</main>


<style>

	input + label{
		display: inline-flex;	
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