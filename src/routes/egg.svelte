<script>
    export let source = "src/img/olive.png";
    export let eggName = "Burford Brown";
</script>
<div class="egg">
    <img src={source} alt="egg">
    <div class="container">
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
      width: 8%;
      float: left;
      margin: 10px;
      padding-top: 10px;
      border-radius: 10px;  
      text-align: center;
      background-color: white;
    }
    
    .egg:hover {
      box-shadow: 0 8px 16px 0 rgba(0,0,0,0.5);
    }
    
    .container {
      padding: 2px 4px;
      text-align: center;
    }
    </style>