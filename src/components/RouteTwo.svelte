<script>
    import { useNavigate } from "svelte-navigator";

    // Initial Navigate
    const navigate = useNavigate();

    const handleMove = () => {
        navigate("/");
    };
</script>

<main>
    <h1>Route Two</h1>

    <button on:click={() => handleMove()}>Move to First Route</button>
</main>

<style></style>
