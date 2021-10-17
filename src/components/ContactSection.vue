<template>
    <div class="contact">
        <div class="heading">
            <h1>KONTAKT</h1>
            <p class="subtitle">LEONIDES</p>
            <img src="../assets/ornament.svg" alt="#">
        </div>

        <transition name="show">
            <div v-show="scrollpx > 9750" class="adress">
                <p>ADRESA <i>LEVOČSKÁ 5, PREŠOV, 080 01</i></p>
                <p>TELEFÓN <a href="tel:+421900123456">+421 900 123 456</a></p>
                <p>MESTO <i>PREŠOV / SLOVAKIA</i></p>
                <svg>
                    <line x1="35" y1="0" x2="65" y2="0" stroke="#a39475" />
                </svg>
            </div>
        </transition>

        <div class="contact-form">
            <form id="app" @submit="checkForm" action="https://vuejs.org/" method="post">
                <fieldset>
                    <div class="data-message">
                        
                        <transition name="show-second">
                            <div v-show="scrollpx > 9750" class="data">
                                <label for="name">MENO <input v-model="name" type="text" name="name" id="name"></label>
                                <label for="email">EMAIL <input v-model="email" type="email" name="email" id="email"></label>
                                <label for="phone">TELEFÓN <input v-model="phone" type="text" name="phone" id="phone"></label>
                                <ul v-if="errors.length" class="valid">
                                  <li v-for="( error, index ) in errors" :key="index">{{ error }}</li>
                                </ul>
                            </div>
                        </transition>

                        <transition name="show-third">
                            <div v-show="scrollpx > 9750" class="message">
                                
                                <textarea placeholder="ODKAZ..." name="message" id="message"></textarea>
                            </div>
                        </transition>
                    </div>

                    <transition name="show-fourth">
                    <div v-show="scrollpx > 9750" class="submit">
                        <button type="submit" value="Submit" id="submit">ODOSLAŤ</button>
                    </div>
                    </transition>
                </fieldset>
            </form>
        </div>
        <div class="logo">
            <img src="../assets/logo-head.svg" alt="">
            <img src="../assets/ornament.svg" alt="">
            <p>Copyright 2021</p>
            <p>Všetky práva vyhradené.</p>
        </div>

    </div>
</template>

<script>


    export default {
        name: "ContactSection",

      data () {
        return {
          scrollpx: 0,
          errors: [],
          name: null,
          email: null,
          phone: null
        }
      },

   

    methods: {
      handleScroll() {
        this.scrollpx = window.scrollY;
      },

      checkForm: function (e) {
        this.errors = [];

        if (!this.name) {
          this.errors.push("Name required.");
        }

        if (!this.phone) {
          this.errors.push("Phone required.")
        }

        if (!this.email) {
          this.errors.push('Email required.');
        } 
        
        else if (!this.validEmail(this.email)) {
          this.errors.push('Valid email required.');
        }

        if (!this.errors.length) {
          return true;
        }

      e.preventDefault();
    },
    validEmail: function (email) {
      var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    }

    },

        created() {
            window.addEventListener('scroll', this.handleScroll);
        },
        
        destroyed() {
            window.removeEventListener('scroll', this.handleScroll);
        },

    }
</script>

<style lang="scss" scoped>

    $mainColor: #a39475;


    .contact {
        background: url('../assets/bg-contact.svg') no-repeat;
        background-size: cover;
        position: relative;
        z-index: 16;
        padding-bottom: 50px;
        
    }

    .heading {
        display: inline-block;
        margin:460px 0 100px 0;

        h1 {
            font-size: 2em;
            margin: 0;
        }

        .subtitle {
            margin: 0;
            color: $mainColor;
        }
  }

    
    img {
        width: 200px;
        height: auto;
  }

    .adress {
        margin-bottom: 100px;
    }

    .adress p {
        font-weight: 900;
    }

    .adress i {
        color: $mainColor;
        font-weight: bold;
        font-style: normal;
    }

    .adress a {
        color: $mainColor;
        font-weight: bold;
        text-decoration: none;
    }

    svg {
        width: 100px;
        height: 10px;
        stroke-width: 5px;
        margin-top: 10px;
  }

    fieldset {
      border: none;
      padding: 0;
      margin: 0;
  }

    .data {
      display: flex;
      flex-direction: column;
      width: 575px;
      margin-right: 50px;
  }

  .message {
      display: flex;
      
  }

  .data label {
      margin-bottom: 30px;
  }

  .data :last-child {
      margin-bottom: 0;
  }

    .data-message {
      display: flex;
      flex-direction: row;
      margin-bottom: 100px;
  }

    .contact-form {
      max-width: 1200px;
      margin: 0 auto 300px auto;
  }

    input {
        border: none;
        background: none;
        outline: none;
  }

    label {
      border-bottom: 1px solid grey;
      text-align: left;
     
  }

    textarea {
      background: none;
      outline: none;
      resize: none;
      border-radius: 2px;
      width: 575px;
  }

  button {
      border: none;
      background: none;
      cursor: pointer;
  }

  .submit {
      border-bottom: 1px solid grey;
      padding: 20px 0;
      cursor: pointer;
      &:hover {
          border-bottom: 4px solid $mainColor;
          transition: .2s;
      }
  }

  .logo {
      display: flex;
      flex-direction: column;
      align-items: center;
  }

  p {
      margin: 0;
  }

  .valid {
    position: absolute;
    display: flex;
    flex-direction: column;
    list-style-type: none ;
    margin: 0;
    padding-left: 200px;
    
    li {
      padding-bottom: 25px;
      color: red;
      font-weight: bold;
    }
  }

  .show-enter-active {
    transition: all 0.4s ease-in;
  }

  .show-enter-from {
    transform: translateY(50vh);
  }

  .show-second-enter-active {
    transition: all 0.7s ease-in;
  }

  .show-second-enter-from {
    transform: translateY(50vh);
  }

  .show-third-enter-active {
    transition: all 1s ease-in;
  }

  .show-third-enter-from {
    transform: translateY(50vh);
  }

  .show-fourth-enter-active {
    transition: all 1.3s ease-in;
  }

  .show-fourth-enter-from {
    transform: translateY(50vh);
  }

</style>