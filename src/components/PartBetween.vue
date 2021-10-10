<template>
    <div class="between">
        <img class="head" src="../assets/head.svg" alt="head">
        <img class="circles" src="../assets/bg-needs-circles.svg" alt="circle">  
        <div class="motto">
            <h3>LEONIDES</h3>
            <p>Transform your life!</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'PartBetween'
    }
</script>

<style lang="scss" scoped>
    .between {
        height: 300px;
    
    }

    .head {
        display: block;
        position: relative;
        top: -60px; 
        left: 0px;
        width: auto;
        height: 600px;
        z-index: 9;
    }

    .circles {
        display: block;
        position: relative;
        top: -615px; 
        left: 30px;  
        width: auto;
        height: 850px;
        z-index: 10;
        transform: rotate(-4deg);
    }

    .motto {
        display: block;
        position: relative;
        top: -1250px;
        color: #fff;
    }

    h3 {
        font-size: 3em;
        font-weight: bold;
        margin: 0;
    }

    p {
        letter-spacing: 4px;
        word-spacing: 5px;
        margin: 0;
    }
</style>