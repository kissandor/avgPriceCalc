<script lang="ts">
    import Egg from "./egg.svelte";
    let eggs = [
        {name: 'Olive', source: '/src/routes/olive.png'},
        {name: 'Leghorn', source: './src/img/leghorn.png'},
        {name: 'Legbar', source: './src/img/legbar.png'},
        {name: 'Burfordd', source: './src/img/burford.png'},
        ]
</script>


<div class="container">
    <h1>Average egg price calculator</h1>
    {#each eggs as egg}
        <Egg source={egg.source} eggName={egg.name}/>
    {/each}
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
</style>