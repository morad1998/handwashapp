<script>
    import Prgressw from './prgressw.svelte';
    const totalSeconds = 20;
    let secondsLeft = totalSeconds;
    let isRunning = false;
    $: progress = (((totalSeconds-secondsLeft)/totalSeconds)*100);


    function clickTimer(){
        isRunning = true;
        const timer = setInterval(() => {
       secondsLeft -= 1;
       if(secondsLeft == 0){
           clearInterval(timer);
           isRunning = false;
           secondsLeft = totalSeconds;
       } 
    }, 1000);

    }

    

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

    .start[disabled]{
        background-color: gray;
        cursor: not-allowed;
    }
</style>

<div bp="grid">
    <h2 bp="offset-5@md 4@md @12@sm">Seconds Left: {secondsLeft}</h2>
</div>

<Prgressw {progress}/>
<button disabled={isRunning} bp="offset-5@md 4@md @12@sm" class="start" on:click={clickTimer}>Start</button>