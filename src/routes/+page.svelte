<script lang="ts">
    import Egg from "./egg.svelte";
    import Calc from "./calculator.svelte";
    import Box from "./result.svelte";
    let eggNameProfile: string = "Burford";
    let eggs = [
        {name: 'Olive', source: '/src/img/olive.png', size: [4, 37, 43, 6, 4, 6]},
        {name: 'Legbar', source: '/src/img/legbar.png', size: [2, 22, 64, 5, 2, 5]},
        {name: 'Burford', source: '/src/img/burford.png', size: [3, 40, 41, 4, 2, 10]},
        {name: 'Leghorn', source: '/src/img/leghorn.png', size: [2, 51, 40, 2, 2, 3]},
        {name: 'White FR', source: '/src/img/whitefr.png', size: [2, 51, 40, 2, 2, 3]},
        {name: 'OF+G', source: '/src/img/ofg.png',size: [3, 41, 45, 4, 2, 5]},
        {name: 'BBT SA', source: '/src/img/sa.png', size: [3, 51, 35, 4, 2, 5]},
        {name: 'BBT', source: '/src/img/bbt.png', size: [3, 43, 43, 4, 2, 5]},
        {name: 'Woodland', source: '/src/img/woodland.png', size: [3, 40, 46, 3, 3, 5]},
        {name: 'Free Range', source: '/src/img/freerange.png', size: [3, 41, 45, 4, 2, 5]},
        ];
    
       let profifile2:number[] = [0,0,0,0,0,0];
        
        function handleMessage(event: { detail: { text: any; }; }) {
		    eggNameProfile =  (event.detail.text).toString();
            
            const egg = eggs.find((egg) => egg.name.toLowerCase() === eggNameProfile.toLowerCase());
            if (egg){
                profifile2 = egg.size;
            }
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
            <Calc profile= {profifile2}/>
        </div>
        <div class="res">
            <span>
                <Box>
                    <h2>Hello!</h2>
                    <p>This is a box. It can contain anything.</p>
                </Box>
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
        height: 100vh;
        padding: 0px 50px;
        background-color: #F5F4F3;
        box-sizing: border-box;
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