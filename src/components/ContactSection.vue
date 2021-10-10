<template>
    <div class="contact">
        <div class="heading">
            <h1>KONTAKT</h1>
            <p class="subtitle">LEONIDES</p>
            <img src="../assets/ornament.svg" alt="#">
        </div>
        <div class="adress">
            <p>ADRESA <i>LEVOČSKÁ 5, PREŠOV, 080 01</i></p>
            <p>TELEFÓN <a href="tel:+421900123456">+421 900 123 456</a></p>
            <p>MESTO <i>PREŠOV / SLOVAKIA</i></p>
            <svg>
                <line x1="35" y1="0" x2="65" y2="0" stroke="#a39475" />
            </svg>
        </div>
        <div class="contact-form">
            <form action="#" method="POST">
                <fieldset>
                    <div class="data-message">
                        <div class="data">
                            <label for="name">MENO <input type="text" name="name" id="name"></label>
                            <label for="email">EMAIL <input type="text" name="email" id="email"></label>
                            <label for="phone">TELEFÓN <input type="text" name="phone" id="phone"></label>
                        </div>
                
                        <div class="message">
                            
                            <textarea placeholder="ODKAZ..." name="message" id="message"></textarea>
                        </div>
                    </div>

                    <div class="submit">
                        <button type="submit" id="submit">ODOSLAŤ</button>
                    </div>
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
        name: "ContactSection"
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
        margin: 400px 0 100px 0;

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
  }

  .submit {
      border-bottom: 1px solid grey;
  }

  .logo {
      display: flex;
      flex-direction: column;
      align-items: center;
  }

  p {
      margin: 0;
  }

</style>