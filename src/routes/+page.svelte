<script lang="ts">
    import Egg from "./egg.svelte";
    import Calc from "./calculator.svelte";
    import Dispay from "./result.svelte";
    let eggNameProfile: string = "Burford";
    let price: number[] = [0,0,0,0,0,0];

    let eggs = [
        {name: 'Olive', source: 'olive.png', size: [4, 37, 43, 6, 4, 6]},
        {name: 'Legbar', source: 'legbar.png', size: [2, 22, 64, 5, 2, 5]},
        {name: 'Burford', source: 'burford.png', size: [3, 40, 41, 4, 2, 10]},
        {name: 'Leghorn', source: 'leghorn.png', size: [2, 51, 40, 2, 2, 3]},
        {name: 'White FR', source: 'whitefr.png', size: [2, 51, 40, 2, 2, 3]},
        {name: 'OF+G', source: 'ofg.png',size: [3, 41, 45, 4, 2, 5]},
        {name: 'BBT SA', source: 'sa.png', size: [3, 51, 35, 4, 2, 5]},
        {name: 'BBT', source: 'bbt.png', size: [3, 43, 43, 4, 2, 5]},
        {name: 'Woodland', source: 'woodland.png', size: [3, 40, 46, 3, 3, 5]},
        {name: 'Free Range', source: 'freerange.png', size: [3, 41, 45, 4, 2, 5]},
        ];
    
    let profifile2:number[] = [0,0,0,0,0,0];
        
    function handleMessage(event: { detail: { text: any; }; }) {
		    eggNameProfile =  (event.detail.text).toString();
            
            const egg = eggs.find((egg) => egg.name.toLowerCase() === eggNameProfile.toLowerCase());
            if (egg){
                profifile2 = egg.size;
            }
	    }
    $: avgPrice =   (price.reduce((acc, num, i) => acc + num * profifile2[i], 0) / 10000).toFixed(2);
    $: console.log(avgPrice)

    function priceUpdate(event: { detail: number[]; }){
        price = event.detail
    }

</script>


<div class="container">
    <h1>Average egg price calculator</h1>
    <div class="eggContainer">
        {#each eggs as egg}
            <Egg source={egg.source} eggName={egg.name} on:eggName={handleMessage}/>
        {/each}
    </div>
    <div style="display: flex">
        <div class="calc">
            <Calc profile= {profifile2} on:sendNewPrice={priceUpdate} /> 
        </div>
        <div class="res">
            <span>
                <Dispay avgEggPrice={avgPrice}/>
            </span>
        </div>
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
        height: 100%;
        padding: 0px 50px;
        background-color: #F5F4F3;
        box-sizing: border-box;
        justify-content: center;
        
    }

    .calc{
       width: 35%;
       border: 1px solid rgb(215, 219, 219);
       display: unset;
    }
    
    .res{
        width: 65%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>