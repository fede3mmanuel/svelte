<script>
	let fruits = [
		{name: "Apple", color: "Red", amount: 5, id: 1},
		{name: "Banana", color: "yellow", amount: 7, id: 2},
		{name: "Grape", color: "Purple", amount: 3, id: 3}
	];

	const deleteFruit = (id) => {
		console.log(id);

		fruits = fruits.filter((fruit) => fruit.id != id);

		console.log(fruits);
	}

	let num = 10;

</script>

<main>

	{#each fruits as fruit (fruit.id)}
		{#if fruit.amount < 4}
			<div class="card">
				<h5>{fruits[0].name}</h5>
				<p>{fruits[0].color}</p>
				<button on:click={() => deleteFruit(fruit.id)}>Delete</button>
			</div>
		{:else}
			<p>The amount is {fruit.name} is equal or more than 4</p>
		{/if}
	{:else}
		<p>There is no fruit on our fruit array</p>
	{/each}
</main>

<style>
	h5, p {
		margin: 4px 0px;
	}
	.card {
		max-width: 400px;
		padding: 8px;
		border-radius: 20px;
		border: 2px solid red;
		margin-top: 8px;
	}
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