<template>
    <div class="book">
        <span class="page turn1"></span>
        <span class="page turn2"></span>
    </div>
</template>

<script>
    export default {
        name: "OpenPage"
    }
</script>

<style lang="scss" scoped>


.book {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  width: 18.5rem;
  height: 12.5rem;
  perspective: 70rem;
}
.page {
  background-color: #36354e;
  transform: rotateY(90deg);
  width: 9.25rem;
  height: 12.5rem;
  position: absolute;
  padding: 1rem;
  transform-origin: 100% 0;
  border-radius: 5px 0 0 5px;
  box-shadow: inset 3px 0px 20px rgba(0, 0, 0, 0.2),
   0px 0px 15px rgba(0, 0, 0, 0.1);
  box-sizing: border-box;
}



.page.turn2 {
  animation: secondPage 8s forwards;
  
}

.page.turn1 {
  
  animation: firstPage 8s forwards;
}


@keyframes secondPage {
  30% { z-index: 999 }
  100% {  transform: rotateY(180deg);
    z-index: 1;}
}

@keyframes firstPage {
  30% { z-index: 999 }
  100% {  transform: rotateY(0deg);
    z-index: 1;}
}
</style>