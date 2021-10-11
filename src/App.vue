<template>
  
    
  <div class="first">
    <Nav-main v-if="hiding" @click-button="showMenu(true), hideNav(false)" />
  </div>

  <MenuComponent v-if="showing" @click-button="showMenu(false), hideNav(true)"/>
    
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
      showing: false,
      hiding: true
    }
  },

  methods: {
    showMenu(showing) {
      this.showing = showing
    },

    hideNav(hiding) {
      this.hiding = hiding
    }

  },
  
}


</script>

  

<style lang="scss" scoped>
  
  .first {
    height: 100vh;
  }

 
  
</style>