<template>
    <footer>

      <section id="footer-buy">
        <div class="buy-comics" v-for="activity, i in activitiesBuy" :key="i">
          <img :src="activity.img" :alt="activity.text">
          <span>{{activity.text}}</span>
        </div>
      </section>

      <section id="footer-menu">

        <nav>
          <div id="left-menu">
              <h3>DC COMICS</h3>
            <ul>
              <li>Characters</li>
              <li>Comics</li>
              <li>Movies</li>
              <li>TV</li>
              <li>Games</li>
              <li>Videos</li>
              <li>News</li>
            </ul>

              <h3>SHOP</h3>
            <ul>
              <li>Shop DC</li>
              <li>Shop DC Collectibles</li>
            </ul>
          </div>
          <div id="center-menu">
            <h3>DC</h3>
            <ul>
              <li>Terms of Use</li>
              <li>Privacy policy (New)</li>
              <li>Ad Choices</li>
              <li>Advertising</li>
              <li>Jobs</li>
              <li>Subscriptions</li>
              <li>Talent Workshops</li>
              <li>CPSC Certificates</li>
              <li>Ratings</li>
              <li>Shop Help</li>
              <li>Contact Us</li>
            </ul>
          </div>
          <div id="right-menu">
            <h3>SITES</h3>
            <ul>
              <li>DC</li>
              <li>MAD Magazine</li>
              <li>DC Kids</li>
              <li>DC Universe</li>
              <li>DC Power Visa</li>
            </ul>   
          </div> 
        </nav>

        <div id="logo-footer">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>

      </section>

      <section id="footer-contacts">

        <div class="sign-up">SIGN-UP NOW!</div>
        <div class="socials">
          <span>FOLLOW US</span>
          <img v-for="social, i in socials" :key="i" :src="social">
        </div>
      </section>

    </footer>
</template>

<script>
export default {
  name: 'Footer',
  data(){
    return {
      activitiesBuy: [
        {
          img: "../assets/img/buy-comics-digital-comics.png",
          text: "DIGITAL COMICS"
        },
        {
          img: "../assets/img/buy-comics-merchandise.png",
          text: "DC MERCHANDISE"
        },
        {
          img: "../assets/img/buy-comics-subscriptions.png",
          text: "SUBSCRIPTION"
        },
        {
          img: "../assets/img/buy-comics-shop-locator.png",
          text: "COMIC SHOP LOCATOR"
        },
        {
          img: "../assets/img/buy-dc-power-visa.svg",
          text: "DC POWER VISA"
        }
      ],
      socials: ["../assets/img/footer-facebook.png", "../assets/img/footer-twitter.png", "../assets/img/footer-youtube.png", "../assets/img/footer-pinterest.png", "../assets/img/footer-periscope.png"]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#footer-buy {
  height: 150px;
  background-color: #0282f9;
  color: #fff;
  display: flex;
  justify-content: center;
    .buy-comics {
      display: flex;
      align-items: center;
      margin: 0 10px;
    }
}

#footer-menu {
  background-image: url("../assets/img/footer-bg.jpg");
  display: flex;
  justify-content: space-around;

    nav {
      padding: 45px 0;
      display: flex;
      
        div {
          margin: 0 10px;
        }
      
    }

    h3 {
      color: white;
      margin-bottom: 10px;
    }

    ul {
      list-style-type: none;
      margin-bottom: 10px;
    }

    li {
      color: #5b6f7b;
      margin: 2px 0;
    }
}

#logo-footer {
  img {
    width: 600px;
    height: 375px;
    object-fit: none;
  }

}

#footer-contacts {
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: #303030;
  padding: 30px 0;

    .sign-up {
      padding: 10px 20px;
      color: #fff;
      border: 1px solid #0282f9;
    }

    .socials {
      color: #0282f9;
      font-size: 20px;
    }
}
</style>
