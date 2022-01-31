<script>
    // Components
    import GroceryItem from "./GroceryItem.svelte";

    export let groceries;
</script>

<main>
    <h2>GroceryList</h2>

    <ol>
        {#each groceries as grocery (grocery.id)}
            <GroceryItem>
                <li>{grocery.name}</li>
            </GroceryItem>
        {/each}
    </ol>
</main>

<style></style>
