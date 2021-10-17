<template>
  
    
  <div class="first">
    <transition-group name="hide">
    <Nav-main v-if="hiding" @click-button="showMenu(true), hideNav(false)" />
    </transition-group>
  </div>

  <transition name="show">
    <MenuComponent v-if="showing" @click-button="showMenu(false), hideNav(true)"/>
  </transition>

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

  .show-enter-active {
    transition: all 0.5s ease-in;
  }

  .show-leave-active {
    transition: all 0.8s ease-out;
  }

  .show-enter-from,
  .show-leave-to {
    transform: translateX(-50vw);
  }

  .hide-enter-active {
    transition: all 0.8s ease-in;
  }

  .hide-leave-active {
    transition: all 0.8s ease-out;
  }

  .hide-enter-from,
  .hide-leave-to {
    transform: translateY(-150px);
  }
</style>