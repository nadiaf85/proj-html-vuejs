<template>
  <footer>
    <div class="container_footer">
      <div class="info_footer">
        <ul v-for="(element, index) in categories" :key="index">{{element.text}}
          <li v-for="(element, index) in categories[index].content" :key="index">{{element.text}}</li>
          <li :class=(element.image)></li>
        </ul>
      </div>
      <Logo/>

      <div class="information">
        <h1>Stay In The Loop</h1>
        <h5>Sign up to receive up to date news and offer directly in your inbox:</h5>
        <input type="text" placeholder="you@email.com">
      </div>

      <div class="sub">
        <button>Subscribe</button>
      </div>

      <div class="social">
        <i class="fab fa-facebook"></i>
        <i class="fab fa-twitter"></i>
        <i class="fab fa-instagram"></i>
        <i class="fab fa-linkedin"></i>
        <i class="fas fa-rss"></i>
        <i class="fab fa-youtube"></i>
        <i class="far fa-envelope"></i>
      </div>

      <div class="copyright">
        <p>© Copyright 2012-2020|Avada Theme by Theme Fusion|All Right Reserved|Powered by WordPress</p>
      </div>
    </div>
  </footer>
</template>

<script>
import Logo from '../commons/Logo.vue';

export default {
    name: 'Footer',
    components: {
      Logo
    },
    data() {
    return{
      categories:[
          {
          text: "Order online",
          content:[
            {
              text: "Appetizers"
            },
            {
              text: "Burgers"
            },
            {
              text: "Pizza"
            },
            {
              text: "Fries"
            },
            {
              text: "Sides"
            },
            {
              text: "Desserts"
            },
            {
              text: "Beverages"
            },
            {
              text: "Specials"
            },
          ]
          },
          {
          text: "Navigate",
          content:[
            {
              text: "Home",
              current: true,
            },
            {
              text: "Alternate Home"
            },
            {
              text: "Menu"
            },
            {
              text: "About"
            },
            {
              text: "News"
            },
            {
              text: "Contact Us"
            },
            {
              text: "Cart"
            },
          ]
          },
          {
          text: "Information",
          content:[
            {
              text: "My Account"
            },
            {
              text: "Terms Of Service"
            },
            {
              text: "Privacy Policy"
            },
            {
              image: require ("../../assets/images/app-store-badge.png"),
            },
            {
              image: require ("../../assets/images/play-store-badge.png"),
            },
          ]
          },
          {
          text: "Opening Hours",
          content:[
            {
              text: "Mon - 10AM to 11PM"
            },
            {
              text: "Tue - 10AM to 11PM"
            },
            {
              text: "Wed - 10AM to 11PM"
            },
            {
              text: "Thur - 10AM to 11PM"
            },
            {
              text: "Fri - 10AM to 11PM"
            },
            {
              text: "Sat - 10AM to 11PM"
            },
            {
              text: "Sun - 10AM to 11PM"
            },
          ]
          },
          {
            text: "Voucher",
            content: [
              {
                image: require ("../../assets/images/footer-coupon-200x200.png"),
                text: "Just Use The Code FIRSTORDER At Checkout"
              }
            ]
          }
          
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

footer{
  height: 1000px;
  background-image: url('../../assets/images/footer-background-scaled.jpg');
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
}

.container_footer{
  width: 100%;
  padding: 20px;
}

.info_footer{
  display: flex;
  justify-content: space-evenly;
  width: 100%;
  height: 100%;
  margin-top: 60px;
  
  img{
    width: 80%;
  }
  ul{
    width: 8%;
    color: white;
    list-style: none;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 13px;
    margin-bottom: 15px;

    li{
      color: lightgray;
      text-transform: capitalize;
      font-size: 11px;
      margin: 4px 0;
      font-weight: 200;
      }
    }
  }

// .active{
//       color: $textBigColor;
//       padding-bottom: 20px;
//   }

.logo{
    display: flex;
    justify-content: center;
    margin-top: 50px;
}

.information{
  width: 100%;
  color: white;
  text-align: center;
  line-height: 35px;
  margin-top: 30px;

    h1{
      color: $textBigColor;
    }

  input{
    width: 32%;
    border-radius: 20px;
    padding: 10px;
  }
}

.sub{
  text-align: center;

  button{
    width: 32%;
    border-radius: 20px;
    padding: 8px;
    margin-top: 20px;
    background-color: $buttonColor;
    color: $textColor;
    border: 1px solid $buttonColor;
    text-transform: uppercase;
  }
}

.social{
  color: $textColor;
  text-align: center;
  margin-top: 30px;

  i{
    padding: 20px;
  }
}

.copyright{
  color: $textColor;
  text-align: center;
  margin-top: 30px;
  font-size: 12px
}

</style>