<script>
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher();

    let name = "";

    const handleSubmit = () => {
        dispatch("add-grocery", name);
        name = "";
    };
</script>

<main>
    <form on:submit|preventDefault={handleSubmit}>
        <label for="name">Add an Item</label>
        <input id="name" type="text" bind:value={name} />
    </form>
</main>

<style></style>
