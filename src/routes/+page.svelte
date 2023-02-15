<script lang="ts">
    import Egg from "./egg.svelte";
    let eggs = [
        {name: 'Olive', source: 'public/olive.png'},
        {name: 'Leghorn', source: '/img/leghorn.png'},
        {name: 'Legbar', source: './img/legbar.png'},
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