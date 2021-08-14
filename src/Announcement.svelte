<script>
    let show = true;

    const hideAlert = () => {
        show = false;
    }
</script>

{#if show}
    <div class="alert">
        50% of all fruit, but more
        <button on:click={hideAlert}>Hide</button>
    </div>
{/if}

<style>
    .alert {
        padding: 8px;
        font-size: 18px;
        background-color: darkseagreen;
        color: darkslategray;
    }
</style>