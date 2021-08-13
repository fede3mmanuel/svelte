<script>
// const { text }=require("svelte/internal");

	let name = "";
	let src = "favicon.png";
	let count = 0;

	const incrementCounter = () => {
		count += 1;
	}

	const handleInput = (event) => {
		name = event.target.value;
	}
	const changetoUnknown = () => {
		name = "Unknown";
	}
</script>

<main>
	<h1>Hellodfds {name}</h1>

	<!-- <input type="text" on:input={handleInput} value={name}> -->

	<input type="text" bind:value={name}>

	<button on:click={changetoUnknown}>changetoUnknown</button>

	<!-- <h3>Counter: {count}</h3>
	<button on:click={incrementCounter}>Add 1 to counter</button> -->
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