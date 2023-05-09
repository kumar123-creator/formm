<script>
	export let firstName = "";
	export let lastName = "";
	export let email = "";
	
	function handleSubmit() {
	  const formData = {
		firstName,
		lastName,
		email,
	  };
	  console.log(formData);
	}
  </script>
  
  <form on:submit|preventDefault={handleSubmit}>
	<label>
	  First Name:
	  <input type="text" bind:value={firstName} required />
	</label>
	
	<label>
	  Last Name:
	  <input type="text" bind:value={lastName} required />
	</label>
	
	<label>
	  Email:
	  <input type="email" bind:value={email} required />
	</label>
	
	<button type="submit">Submit</button>
  </form>
