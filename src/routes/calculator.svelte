<script lang="ts">
   export let profile:number[] = [0, 0, 0, 0, 0, 0];
</script>

<div class="calculator">
    <div class="firstRow">
        <div class="size"></div>
        <span class="profile">Grades %</span>
        <span class="">Pence/Doz</span>
        
    </div>
    <div class="row">
        <div class="size">Very Large</div>
        <label class="profile" for="vl">{profile[0]}%</label>
        <input class="inputPrice" type="text" id="vl">
    </div>
    <div class="row">
        <div class="size">Large</div>
        <label class="profile" for="lrg">{profile[1]}%</label>
        <input class="inputPrice" type="text" id="lrg">
    </div>
    <div class="row">
        <div class="size">Medium</div>
        <label class="profile" for="med">{profile[2]}%</label>
        <input class="inputPrice" type="text" id="med">
    </div>
    <div class="row">
        <div class="size">Smalls</div>
        <label class="profile" for="sml">{profile[3]}%</label>
        <input class="inputPrice" type="text" id="sml">
    </div>
    <div class="row">
        <div class="size">Graded seconds</div>
        <label class="profile" for="gs">{profile[4]}%</label>
        <input class="inputPrice" type="text" id="gs">
    </div>
    <div class="row">
        <div class="size">Farm seconds</div>
        <label class="profile" for="fs">{profile[5]}%</label>
        <input class="inputPrice" type="text" id="fs">
    </div>
</div>

<style>
    .calculator{
        font-size: 1vw;
    }
    .firstRow{
        padding: 17px;
        box-sizing: border-box;
    }
    .row{
        border-top: 1px solid rgb(215, 219, 219);
        padding: 17px;
        box-sizing: border-box;
    }

    .size{
        display: inline-block;
        width: 30%;
        margin-right: 20px;
    }
    
    .profile{
        display: inline-block;
        width: 20%;
        margin-right: 40px;
    }

    input[type=text] {
        width: 20%;
        padding: 8px 10px;
        box-sizing: border-box;
    }

</style>