<template>
  <div class="nav" @scroll="handleSCroll">
    <ul class="nav-left">
      
      <li>
        <a class="nav-link" href="#">
          <svg class="svg1">
            <line x1="0" y1="0" x2="100" y2="0" stroke="#a39475" />
          </svg>
          01
        </a> 
      </li>

      <li>
        <a class="nav-link" href="#">
          <svg class="svg2">
            <line x1="0" y1="0" x2="100" y2="0" stroke="#a39475" />
          </svg>
          02
        </a> 
      </li>

      <li>
        <a class="nav-link" href="#">
          <svg class="svg3">
            <line x1="0" y1="0" x2="100" y2="0" stroke="#a39475" />
          </svg>
          03
        </a> 
      </li>

    </ul>

    <a @click.prevent="sendEvent" class="menu-button" href="#">
      MENU
      <img src="../assets/menu.svg" alt="menu">
    </a>

    <ul class="nav-right">
      
      <li>
        <a class="nav-link" href="#">
          <svg class="svg4">
            <line x1="0" y1="0" x2="110" y2="0" stroke="#a39475" />
          </svg>
          04
        </a> 
      </li>

      <li>
        <a class="nav-link" href="#">
          <svg>
            <line x1="0" y1="0" x2="110" y2="0" stroke="#a39475" />
          </svg>
          05
        </a> 
      </li>

      <li>
        <a class="nav-link" href="#">
          <svg>
            <line x1="0" y1="0" x2="110" y2="0" stroke="#a39475" />
          </svg>
          06
        </a> 
      </li>

    </ul>
  </div>
</template>

<script>
  export default {
    name: 'NavMain',


       methods: {
        sendEvent(e) {
          this.$emit('click-button')
        },

        handleSCroll (event) {
          let svg1 = document.querySelector(".svg1");
          let svg2 = document.querySelector(".svg2");
          let svg3 = document.querySelector(".svg3");
          let svg4 = document.querySelector(".svg4");
          
          if (window.scrollY > 600 ) {
          console.log(window.scrollY);
          svg1.classList.add("svg-scroll");          
          }
  
          else {
            svg1.classList.remove('svg-scroll')
          }

          if (window.scrollY > 3300 ) {
            svg1.classList.remove('svg-scroll')
            svg2.classList.add('svg-scroll')
          }

          else {
            svg2.classList.remove('svg-scroll')
          }

          if (window.scrollY > 6100 ) {
            svg2.classList.remove('svg-scroll')
            svg3.classList.add('svg-scroll')
          }

          else {
            svg3.classList.remove('svg-scroll')
          }

          if (window.scrollY > 9200 ) {
            svg3.classList.remove('svg-scroll')
            svg4.classList.add('svg-scroll')
          }

          else {
            svg4.classList.remove('svg-scroll')
          }
        }
    },
        created () {
          window.addEventListener('scroll', this.handleSCroll);

        },
        destroyed () {
          window.removeEventListener('scroll', this.handleSCroll);
        } 
    }
    
</script>

<style lang="scss" scoped>

  $mainColor:#a39475;


    .nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 25px;
    z-index: 100;
  }

 
  .nav-left {
    list-style-type: none;
    padding: 0;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 600px;
    list-style-type: none;
    text-align: left;
    
  }

  .nav-right {
    list-style-type: none;
    padding: 0;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 600px;
    text-align: right;
    
  }

  .nav-link {
    text-decoration: none;
    color: $mainColor;
    display: flex;
    flex-direction: column;
  }


  .menu-button {
    display: flex;
    flex-direction: column;
    color: $mainColor;
    text-decoration: none;
  }

  svg {
    width: 100px;
    height: 20px;
    stroke-width: 2px;
  }

  .svg-scroll {
    stroke-width: 6px;
    transition: .6s;
    
  }
</style>