<script lang="ts">
    export let source = "olive.png";
    export let eggName = "Burford Brown";

    import { createEventDispatcher } from 'svelte';

	  const dispatch = createEventDispatcher();

	  function changeEggProfile(eggName: String) {
		  dispatch('eggName', {
			  text: eggName
		});
	}
</script>

<div class="egg">
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <img src={source} alt="egg" on:click={()=>{changeEggProfile(eggName)}}>
    <div class="cont">
      <span><b>{eggName}</b></span>  
    </div>
  </div>

<style>
    img{
        width: 85%;
        border-radius: 5px;
    }
    .egg {
      box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
      transition: 0.3s;
      width: 7%;  
      display: inline-block;
      margin: 10px;
      padding-top: 10px;
      border-radius: 10px;  
      text-align: center;
      background-color: white;
    }
  
    .egg:hover {
      box-shadow: 0 0px 8px 3px rgba(0,0,0,0.7);
      cursor: pointer;
    }
    
    .cont {
      padding: 2px 4px;
      text-align: center;
      font-size: 0.9vw;
    }
    </style>