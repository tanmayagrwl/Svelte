<script>
  import { group_outros } from "svelte/internal";

	const formValues = {
		name : '',
		profileSummary: '',
		country:'',
		jobLocation : [],
		remoteWork : false,
		skillSet : [],
		yearsOfExperience:'',
	}
	function submitForm(event){
		event.preventDefault()
		console.log(formValues)

	}
</script>

<main>
	<div>
		<pre>
			{JSON.stringify(formValues,null,2)}
		</pre>
	</div>
	<form on:submit={submitForm}>
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
			<input type="checkbox" name="remoteWork" id="remoteWork" bind:checked={formValues.remoteWork}>
			<label for="remoteWork">Open to remote work</label>
		<div>

			<div>
				<label for="skillSet" >Skill Set</label>
				<input type="checkbox" name="html" id="html" value="html" bind:group={formValues.skillSet}/>
				<label for="html">HTML</label>
				<input type="checkbox" name="css" id="css" value="css" bind:group={formValues.skillSet} />
				<label for="html">CSS</label>
				<input type="checkbox" name="Js" id="Js" value="Js" bind:group={formValues.skillSet}/>
				<label for="html">Js</label>
			</div>

			<div>
				<label for="years-of-experience" >Years of Experience</label>
				<input type="radio" name="html" id="0-2" value="0-2" bind:group={formValues.yearsOfExperience}/>
				<label for="html">0-2</label>
				<input type="radio" name="css" id="3-5" value="3-5" bind:group={formValues.yearsOfExperience} />
				<label for="html">3-5</label>
				<input type="radio" name="Js" id="6+" value="6+" bind:group={formValues.yearsOfExperience}/>
				<label for="html">6+</label>
			</div>

			<div>
				<button>Submit</button>
			</div>

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