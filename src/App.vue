<template>
  
    
  <div class="first">
    <Nav-main @click-button="showMenu(true)"/>
  </div>

  <MenuComponent/>
    
  <AboutCompany/>

  <ImagesSection/>

  <PartBetween/>

  <PeoplesNeeds/>

  <PartBetweenSecond/>

  <ContactSection/>

  
</template>

<script>
import NavMain from "./components/NavMain.vue";
import AboutCompany from './components/AboutCompany.vue';
import ImagesSection from "./components/ImagesSection.vue";
import PartBetween from "./components/PartBetween.vue";
import PeoplesNeeds from "./components/PeoplesNeeds.vue";
import PartBetweenSecond from "./components/PartBetweenSecond.vue";
import ContactSection from "./components/ContactSection.vue";
import MenuComponent from "./components/MenuComponent.vue"


export default {
  name: 'App',
  components: {
    NavMain,
    AboutCompany,
    ImagesSection,
    PartBetween,
    PeoplesNeeds,
    PartBetweenSecond,
    ContactSection,
    MenuComponent
  },
  data() {
    return {
      showing: false
    }
  },

  methods: {
    showMenu(showing) {
      this.showing = showing
      console.log(showing)
    }

  },
  
}


</script>

  

<style lang="scss" scoped>
  
  .first {
    height: 100vh;
  }

 
  
</style>