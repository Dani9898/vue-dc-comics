<template>
    <footer>

      <section id="footer-buy">
        <div class="buy-comics" v-for="activity, i in activitiesBuy" :key="i">
          <img :src="require(`../assets/img/${activity.img}`)" :alt="activity.text">
          <span>{{activity.text}}</span>
        </div>
      </section>

      <section id="footer-menu">

        <nav>
          <div id="left-menu">
              <h3>DC COMICS</h3>
            <ul>
              <li>Characters</li>
              <li>0Comics</li>
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
          <img v-for="social, i in socials" :key="i" :src="require(`../assets/img/${social}`)">
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
          img: "buy-comics-digital-comics.png",
          text: "DIGITAL COMICS"
        },
        {
          img: "buy-comics-merchandise.png",
          text: "DC MERCHANDISE"
        },
        {
          img: "buy-comics-subscriptions.png",
          text: "SUBSCRIPTION"
        },
        {
          img: "buy-comics-shop-locator.png",
          text: "COMIC SHOP LOCATOR"
        },
        {
          img: "buy-dc-power-visa.svg",
          text: "DC POWER VISA"
        }
      ],
      socials: ["footer-facebook.png", "footer-twitter.png", "footer-youtube.png", "footer-pinterest.png", "footer-periscope.png"]
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
      margin: 0 30px;
        img {
          width: 50px;
        }
        
        span {
          margin-left: 15px;
        }
    }
}

#footer-menu {
  background-image: url("../assets/img/footer-bg.jpg");
  display: flex;
  justify-content: space-around;
  height: 400px;

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
    height: 100%;
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
      border: 2px solid #0282f9;
    }

    .socials {
      color: #0282f9;
      font-size: 20px;
      display: flex;
      align-items: center;
        span {
          margin-right: 20px;
        }
        
        img {
          margin: 0 10px;
        }
    }
}
</style>
