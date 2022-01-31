<script>
	import { Router, Route } from "svelte-navigator";

	// Components
	import GroceryList from "./components/GroceryList.svelte";
	import AddGrocery from "./components/AddGrocery.svelte";
	import RouteOne from "./components/RouteOne.svelte";
	import RouteTwo from "./components/RouteTwo.svelte";

	// Groceries
	let groceries = [
		{ id: 1, name: "Milk" },
		{ id: 2, name: "Bread" },
		{ id: 3, name: "Tea" },
	];

	let name = "";
	// let surName = "Skills";

	const updateValues = () => {
		name = "Svelte";
		surName = "Video";
	};

	const addItem = (e) => {
		const newItem = e.detail;

		groceries = [
			...groceries,
			{
				id: Math.random(),
				name: newItem,
			},
		];

		name = "";
	};

	$: count = groceries.length;
</script>

<main>
	<!-- <p>Reactive Count: {count}</p> -->

	<!-- <ol>
		{#each groceries as grocery (grocery.id)}
			<li>
				{grocery.name}
			</li>
		{/each}
	</ol> -->
	<!-- <AddGrocery on:add-grocery={addItem} />
	<GroceryList name="John" {groceries} /> -->

	<Router>
		<Route path="/">
			<RouteOne />
		</Route>
		<Route path="/r2">
			<RouteTwo />
		</Route>
	</Router>
</main>
