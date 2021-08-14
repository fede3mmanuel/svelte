<script>
    export let btnText = "Componenet button";
</script>
<div on:click>
    <span>Click to log</span>
    <button >
        {btnText}
    </button>
</div>

<style>
    button {
        background: #667eaa;
        border: 1px solid #4c51bf;
        color: #fff;
    }
</style>