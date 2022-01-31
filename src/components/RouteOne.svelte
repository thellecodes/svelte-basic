<script>
    import { useNavigate } from "svelte-navigator";

    // Initial Navigate
    const navigate = useNavigate();

    const handleMove = () => {
        navigate("/r2");
    };
</script>

<main>
    <h1>Route One</h1>

    <button on:click={() => handleMove()}>Move to second Route</button>
</main>

<style></style>
