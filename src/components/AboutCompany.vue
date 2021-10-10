<template>
  <div class="about-company">
    <article>
      <div class="heading">
        <h1>O SPOLOČNOSTI</h1>
        <p class="subtitle">LEONIDES</p>
        <img src="../assets/ornament.svg" alt="#">
      </div>
      <section class="section-links">
        <a href="#">
          INŠPIROVANÝ HISTÓRIOU
          <img src="../assets/menu-about-1.jpg" alt="">
        </a>
        <a href="#">
          VÍZIA A POSLANIE
          <img src="../assets/menu-about-2.jpg" alt="">
        </a>
        <a href="#">
          HODNOTY LEONIDES
          <img src="../assets/menu-about-3.jpg" alt="">
        </a>
      </section>
      <section class="section-article">
        <h2>Inšpirovaný históriou</h2>
        <p class="p-article-first">Toffee muffin cookie tart marzipan lemon drops. Chocolate cake bear claw chocolate lemon drops. Cotton candy wafer shortbread pie lemon drops jujubes chocolate cake sweet roll cake. Powder macaroon pie donut sweet roll tiramisu toffee gummies gummi bears. Gummies sesame snaps brownie wafer cotton candy. Bear claw soufflé soufflé sesame snaps gummies dessert. Ice cream tart jelly biscuit powder. Croissant cookie carrot cake soufflé jelly-o biscuit. Chocolate sweet gingerbread sweet brownie soufflé fruitcake. Halvah cake macaroon jelly tart macaroon pastry. Pie fruitcake jelly jelly-o fruitcake muffin pudding sweet. <br>  Bonbon pudding caramels cotton candy brownie. Candy dragée gingerbread chupa chups muffin jelly-o. Chupa chups chocolate cake gummi bears pastry oat cake. Cotton candy cheesecake sesame snaps lollipop marshmallow chocolate cake sweet roll soufflé. Jelly-o cupcake powder cupcake apple pie muffin. Macaroon muffin caramels dessert jelly-o croissant chocolate cake bear claw. Croissant sesame snaps muffin halvah cake candy canes gummies. Soufflé wafer muffin biscuit dessert. Cake cheesecake marzipan cookie soufflé.</p>
        <p class="p-article-second">Marshmallow chocolate gummies cake chocolate cake candy. Brownie sweet roll powder chupa chups jelly beans chocolate cake tart soufflé. Topping biscuit jelly-o gummi bears lemon drops apple pie chocolate cake oat cake. Brownie apple pie croissant lemon drops apple pie candy wafer cupcake. Brownie donut croissant jelly beans sugar plum. Cake jelly beans lemon drops caramels carrot cake pastry wafer candy muffin. Gummi bears topping toffee sugar plum tart liquorice tiramisu cookie gingerbread. Macaroon liquorice lollipop sweet roll sweet bear claw shortbread fruitcake. Liquorice fruitcake brownie halvah tootsie roll. Chocolate cake shortbread donut donut jujubes tart lemon drops cookie. Cake macaroon macaroon donut jelly-o gummi bears fruitcake. Caramels apple pie croissant croissant caramels cake cupcake apple pie dessert. Tart cheesecake danish jelly-o muffin pudding. Cake halvah cake chocolate bar pudding soufflé dragée. Jelly beans gummies wafer icing oat cake. Gummi bears tootsie roll tart muffin tiramisu cheesecake dragée sesame snaps sesame snaps. Sweet sesame snaps dragée dessert marshmallow chocolate sweet roll jujubes. Cotton candy donut carrot cake jelly-o sweet roll. Halvah carrot cake pastry brownie sweet pastry candy liquorice candy. Shortbread lollipop apple pie cake jelly marshmallow. Danish chocolate cake gummi bears liquorice muffin carrot cake tart cake pie.</p>
      </section>
      <section class="section-article">
        <h2>Vízia a poslanie Leonides</h2>
        <p class="p-article-third">Jelly beans cookie wafer topping croissant. Jelly-o donut halvah cheesecake gummies topping caramels sweet roll. Pastry gingerbread tootsie roll chocolate candy canes marzipan cheesecake apple pie gummies. Ice cream cake macaroon halvah toffee fruitcake croissant candy. Soufflé gummies biscuit marzipan marzipan toffee cake dessert. Soufflé sugar plum apple pie cake tart. Pastry cake danish tiramisu bonbon liquorice donut caramels. Lemon drops gummi bears tart biscuit carrot cake. Jujubes tart pudding donut dessert. Gummi bears brownie shortbread danish pie pudding. Caramels chupa chups bonbon ice cream pudding powder. Lemon drops cookie lollipop cheesecake jelly-o gummi bears sweet chocolate cake. Jelly beans soufflé croissant brownie brownie bonbon. Brownie bear claw gummi bears cotton candy powder brownie ice cream liquorice. Dragée bonbon gummi bears wafer shortbread wafer brownie donut. Gummi bears cookie icing chocolate bar dragée pastry cotton candy sweet. Fruitcake muffin cookie dessert gingerbread gummies. Cake pie chocolate icing tootsie roll pudding marzipan carrot cake fruitcake. Soufflé marshmallow sweet roll sesame snaps liquorice. Marshmallow cupcake jujubes macaroon apple pie lollipop pastry pie. Halvah danish sweet roll jelly-o pastry candy marzipan bear claw halvah. Cookie marzipan gummi bears topping jelly gingerbread cotton candy tiramisu lemon drops. Marzipan topping donut topping biscuit soufflé carrot cake pudding chupa chups.</p>
      </section>
      <section class="section-list">
        <h2>Hodnoty</h2>
        <ul>
          <li>Dragée</li>
          <li>Soufflé</li>
          <li>Fruitcake</li>
          <li>Marshmallow</li>
          <li>Marzipan</li>
          <li>Cookie</li>
          <li>Gummi</li>
          <li>Bar</li>
        </ul>
      </section>
      <section class="section-list">
        <h2>Stabilita a zázemie spoločnosti</h2>
        <ul>
          <li>Fruitcake Bar</li>
          <li>Gummi bears cookie icing </li>
          <li>Marzipan Cookie</li>
          <li>Cookie Marzipan</li>
          <li>Soufflé marshmallow sweet roll</li>
          <li>Marzipan topping donut topping</li>
        </ul>
      </section>
      <img class="img-money" src="../assets/money-copy.png" alt="money">
    </article>
  </div>
</template>

<script>
  export default {
    name: 'AboutCompany'
  }
</script>

<style lang="scss" scoped>

$mainColor: #a39475;


  .about-company {
    background: url('../assets/bg-about.svg') no-repeat;
    background-size: cover ;
  }

  article {
    display: inline-block;
    text-align: center;
    max-width: 900px;
    margin-top: 400px;
    margin-bottom: 200px;

    .section-links {
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
      margin-bottom: 100px;
    
      a {
        display: flex;
        flex-direction: column;
        text-decoration: none;
        font-weight: bold;
        color: $mainColor;

        

      }

    
    }

  }

  img {
        width: 200px;
        height: auto;
        }

  .heading {
    margin-bottom: 100px;
    
    h1 {
      font-size: 2em;
      margin: 0;  
    }

    .subtitle {
      margin: 0;
      color: $mainColor;
    }
  }

  

  h2 {
    font-size: 1.2em;
    text-transform: uppercase;
    text-align: left;
    color: $mainColor;
  }


  .p-article-first {
    text-align: justify;
    margin-bottom: 50px;
  }

  .p-article-second {
    text-align: justify;
    margin-bottom: 100px;
  }

  .p-article-third {
    text-align: justify;
    margin-bottom: 100px;
  }

  ul {
    text-align: left;
    list-style-type: none;
    padding: 0;
    margin: 0 0 100px 0;
  }

  .img-money {
    position: absolute;
    margin: -265px 0 0 350px;
  }

  

</style>
