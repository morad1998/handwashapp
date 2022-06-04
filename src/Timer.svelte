<script>
    import Prgressw from './prgressw.svelte'
</script>

<style>
    h2{
        margin: 0px;
    }
    .start{
        background-color: rgb(83, 87, 28);
        width: 100%;
        margin: 10px 0px;
    }
</style>

<div bp="grid">
    <h2 bp="offset-5@md 4@md @12@sm">Seconds Left: </h2>
</div>
<Prgressw/>
<button bp="offset-5@md 4@md @12@sm" class="start">Start</button>