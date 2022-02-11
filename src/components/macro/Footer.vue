<template>
  <footer>
    <div class="container_footer">
      <div class="info_footer">
        <div class="column" v-for="(element, index) in categories" :key="index">
          <h5>{{element.title}}</h5>
          <h6>{{element.text}}</h6>
          <div v-for="(element, index) in categories[index].content" :key="index" :class="{'active': element.current==true}">{{element.text}} 
            <div class="daytime">
              <span class="day">{{element.day}}</span> <span class="time">{{element.time}}</span>
            </div>
          </div>
          <div v-for="(element, index) in categories[index].content" :key="index +'j'"><img :src="element.image" alt=""></div>
        </div>
         <div class="images">
              <img class="img1" src="../../assets/images/app-store-badge-200x67.png" alt="">
              <img class="img2" src="../../assets/images/play-store-badge-200x67.png" alt="">
          </div>
        <div class="voucher">
          <img src="../../assets/images/footer-coupon-200x200.png" alt="">
          Just Use The Code <br> <span class="first">FIRSTORDER</span> <br> At Checkout
        </div>
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
        <span><i class="fab fa-facebook"></i></span>
        <span><i class="fab fa-twitter"></i></span>
        <span><i class="fab fa-instagram"></i></span>
        <span><i class="fab fa-linkedin"></i></span>
        <span><i class="fas fa-rss"></i></span>
        <span><i class="fab fa-youtube"></i></span>
        <span><i class="far fa-envelope"></i></span>
      </div>

      <div class="copyright">
        <p>© Copyright 2012-2020|Avada Theme by <span class="fusion">Theme Fusion</span>Theme by Theme Fusion|All Right Reserved|Powered by <span class="word">WordPress</span></p>
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
          title: "Order online",
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
          title: "Navigate",
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
          title: "Information",
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
          ]
          },
          {
          title: "Opening Hours",
          content:[
            {
              day: "Mon - ",
              time: "10AM to 11PM"
            },
            {
              day: "Tue - ",
              time: "10AM to 11PM"
            },
            {
              day: "Wed - ",
              time: "10AM to 11PM"
            },
            {
              day: "Thur - ",
              time: "10AM to 11PM"
            },
            {
              day: "Fri - ",
              time: "10AM to 11PM"
            },
            {
              day: "Sat - ",
              time: "10AM to 11PM"
            },
            {
              day: "Sun - ",
              time: "10AM to 11PM"
            },
          ]
          },
          {
            title: "Voucher",
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

.active{
      color: $textBigColor;
      padding: 4px;
  }

.info_footer{
  color: white;
  display: flex;
  justify-content: space-evenly;
  position: relative;
  height: 400px;

  .column{
    padding: 20px;
    line-height: 32px;

    h5{
      text-transform: uppercase;
      font-size: 15px;
      margin-bottom: 20px;
    }

    h6{
      font-size: 16px;
    }

    .day{
      font-weight: bold;
    }

    .time{
      color: $textBigColor;
      font-weight: bold;
    }
  }

  .daytime{
    line-height: 21px;
  }

  .images{
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 175px;
    left: 45%;

    .img1{
      border: 1px solid white;
      border-radius: 14px;
      width: 76%;
      left: 15px;
      padding: 3px 3px;
      margin-bottom: 8px;
  }

    .img2{
      border: 1px solid white;
      border-radius: 14px;
      width: 76%;
      left: 15px;
      padding: 0px 3px;
    }
  }

  .voucher{
    position: absolute;
    right: 60px;
    bottom: 292px;
    height: 50px;
    width: 200px;
    text-align: center;

    img{
      width: 84%;
    }

    .first{
      color: $textBigColor;
      font-weight: bold;
    }
  }
}

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

    h5{
      font-weight: 200;
      margin-bottom: 10px;
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
    font-weight: bold;

    &:hover{
      background-color: #bf1e23;
      cursor: pointer;
    }
  }
}

.social{
  color: $textColor;
  text-align: center;
  margin-top: 30px;

  span{
    padding: 5px;
  }
}

.copyright{
  color: $textColor;
  text-align: center;
  margin-top: 30px;
  font-size: 12px;

  p{
    color: $textBigColor;
    font-weight: bold;
  }

  .fusion{
    color: $textColor;
  }

  .word{
    color: $textColor;
  }
}


</style>