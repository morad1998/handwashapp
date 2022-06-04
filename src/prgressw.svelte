<script>
    export let progress = 0;
</script>

<style>
    .progressbar{
        height: 30px;
        background-color: blueviolet;
    }
    .progress-container{
        margin: 20px 0px;
        border: solid rgb(243, 95, 42) 1px;

    }
</style>
<div bp="grid">
    <div class="progress-container" bp="offset-5@md 4@md @12@sm">
        <div style="width: {progress}%;" class="progressbar" bp="offset-5@md 4@md @12@sm">
            <span class="sr-only">%{progress}</span>    

        </div>
    </div>
</div>