<script lang="ts">
    import Egg from "./egg.svelte";
    import Calc from "./calculator.svelte";
    let eggs = [
        {name: 'Olive', source: '/src/img/olive.png'},
        {name: 'Legbar', source: '/src/img/legbar.png'},
        {name: 'Burford', source: '/src/img/burford.png'},
        {name: 'Leghorn', source: '/src/img/leghorn.png'},
        {name: 'White FR', source: '/src/img/whitefr.png'},
        {name: 'OF+G', source: '/src/img/ofg.png'},
        {name: 'BBT SA', source: '/src/img/sa.png'},
        {name: 'BBT', source: '/src/img/bbt.png'},
        {name: 'Woodland', source: '/src/img/woodland.png'},
        {name: 'Free Range', source: '/src/img/freerange.png'},
        ]
</script>


<div class="container">
    <h1>Average egg price calculator</h1>
    <div class="eggContainer">
        {#each eggs as egg}
            <Egg source={egg.source} eggName={egg.name}/>
        {/each}
    </div>
    <div class="calc">
        <Calc />
    </div>
</div>


<style>
    h1{
        text-align: center ;
        padding-top: 5px;
        margin: 0px;
    }
    .container{
        width: 100%;
        height: 100vh;
        padding: 0px 50px;
        background-color: #F5F4F3;
        box-sizing: border-box;
    }

    .calc{
       width: 35%;
       border: 1px solid rgb(215, 219, 219);
    }
    
</style>