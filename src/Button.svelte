<script>
    export let btnText = "Componenet button";
</script>
<div class="card">
    <button on:click|once>
        {btnText}
    </button>
</div>

<style>
    button {
        background: #667eaa;
        border: 1px solid #4c51bf;
        color: #fff;
    }
    .card {
        padding: 12px;
        border: 2px solid gray;
        margin-bottom: 8px;
    }
</style>