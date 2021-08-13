<script>
// const { text }=require("svelte/internal");

	let firstName = "";
	let lastName = "";
	let src = "favicon.png";

	$: fullName = `${firstName} ${lastName}`;
	$: {
		console.log({firstName});
		console.log({lastName});
	}


	const changetoUnknown = () => {
		firstName = "Unknown";
	}
</script>

<main>
	<h1>Hellodfds {fullName}</h1>

	<label for="firstName">firstName</label>
	<input type="text" bind:value={firstName}>

	<label for="LastName">LastName</label>
	<input type="text" bind:value={lastName}>


	<button on:click={changetoUnknown}>changetoUnknown</button>

	<img src={src} alt="Svelte logo">
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	h1 {
		font-size: 72px;
		text-align: center;
	}

	h3 {
		font-size: 30px;
	}
</style>