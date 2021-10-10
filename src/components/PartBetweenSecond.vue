<template>
    <div class="between">
        <img class="circles" src="../assets/bg-contact-circles.svg" alt="circle">  
    </div>
</template>

<script>
    export default {
        name: "PartBetweenSecond"
    }
</script>

<style lang="scss" scoped>

    .between {
        height: 300px;
    }

    .circles {
        display: block;
        position: relative;
        top: 0; 
        left: -133px;  
        width: auto;
        height: 1000px;
        z-index: 13;
    }
</style>