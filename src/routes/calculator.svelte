<script lang="ts">
    let veryLarge = 0;
    let large = 0;
    let medium = 0;
    let smalls = 0;
    let farmSec = 0;
    let gradedSec = 0;
</script>

<div class="calculator">
    <div class="firstRow">
        <div class="size"></div>
        <span class="profile">Grades %</span>
        <span class="">Pence/Doz</span>
        
    </div>
    <div class="row">
        <div class="size">Very Large</div>
        <label class="profile" for="vl">{veryLarge}%</label>
        <input class="inputPrice" type="text" id="vl">
    </div>
    <div class="row">
        <div class="size">Large</div>
        <label class="profile" for="lrg">{large}%</label>
        <input class="inputPrice" type="text" id="lrg">
    </div>
    <div class="row">
        <div class="size">Medium</div>
        <label class="profile" for="med">{medium}%</label>
        <input class="inputPrice" type="text" id="med">
    </div>
    <div class="row">
        <div class="size">Smalls</div>
        <label class="profile" for="sml">{smalls}%</label>
        <input class="inputPrice" type="text" id="sml">
    </div>
    <div class="row">
        <div class="size">Graded seconds</div>
        <label class="profile" for="gs">{gradedSec}%</label>
        <input class="inputPrice" type="text" id="gs">
    </div>
    <div class="row">
        <div class="size">Farm seconds</div>
        <label class="profile" for="fs">{farmSec}%</label>
        <input class="inputPrice" type="text" id="fs">
    </div>
</div>

<style>
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