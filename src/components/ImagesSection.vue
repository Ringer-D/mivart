<template>
    <div class="images">
        <img class="img-1" src="../assets/image01.jpg" alt="">
        <div class="images-grid">
            <div>
            <img class="img-2" src="../assets/image02.jpg" alt="">
            <img class="img-3" src="../assets/image03.jpg" alt="">
            </div>
            <img class="img-4" src="../assets/image04.jpg" alt="">
        </div>
    </div>
    
    
</template>

<script>

    

    export default {
        name: 'ImagesSection',
       
    }
</script>

<style lang="scss" scoped>

    .images {
        line-height: 0;
    }

    .images-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        line-height: 0;
    }    

    .img-1 {
        max-width: 100%;
        height: auto;
    }

    .img-2 {
        max-width: 100%;
        height: auto;
        
    }

    .img-3 {
        position: relative;
        max-width: 100%;
        height: auto;
        z-index: 11;
        
    }

    .img-4 {
        max-width: 100%;
        height: auto;
        
        
    }

</style>