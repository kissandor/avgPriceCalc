<script lang="ts">
	export let avgEggPrice:string;
</script>
<p class="avgText">Avarage egg price:</p>
<p class="display">
	£ {avgEggPrice}
</p>

<style>
	p{
		text-align: center;

	}
	.avgText{
		font-size: 3vw;
		font-weight: bold;
		margin-top: 30px;
	}
	.display{
		font-size: 8vw;
		margin-top: 20px;	
	}
</style>