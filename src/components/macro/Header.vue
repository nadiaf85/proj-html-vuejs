<template>
  <header>
      <div class="container">
            <div class="logo">
                <img src="../../assets/images/takeout-logo.png" alt="">
            </div>
            <nav>
                <ul>
                    <li v-for="(element, index) in info" :key="index">
                    <a href="#" :class="{'active': element.current==true}">{{element.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
        <div class="container_info">
          <div class="text_left">
              <h5>Hungry?</h5>
              <h3>Great Food</h3>
              <p>Delivered</p>
              <button type="button" class="button">View our menu <i class="fas fa-arrow-circle-right"></i></button>
              <!-- <span>Delivered</span> -->
        </div>
      </div>

        <!-- <Delivery/> -->

    </header>
</template>

<script>
// import Delivery from '../commons/Delivery.vue';

export default {
    name: 'Header',
    components:{
      // Delivery
    },
    data() {
      return{
        info: [
            {
                text: "Home",
                url: "#",
                current: false,
            },
            {
                text: "Order online",
                url: "#",
                current: true,
            },
            {
                text: "About",
                url: "#",
                current: false,
            },
            {
                text: "News",
                url: "#",
                current: false,
            },
            {
                text: "Contact us",
                url: "#",
                current: false,
            },
            {
                text: "carrello",
                url: "#",
                current: false,
            }
        ]
      }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

header{
    height: 830px;
    background-image: url('../../assets/images/home-background-hero-scaled.jpg');
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
}

.container{
  display: flex;
  justify-content: space-around;
  align-items: center;
}
  .logo{
    display: flex;
    width: 25%;
    padding: 8px;
  }

nav{
     line-height: 80px;

    ul{
    list-style-type: none;
    display: flex;
    justify-content: center;
    text-transform: uppercase;
    }

    li a{
      display: inline-block;
      color: white;
      padding: 15px 10px;
      text-decoration: none;
      font-size: 12px;
      font-weight: 600;
    }
  }

.container_info{
    width: 80%;
    margin: auto;
}

.text_left{
    color: white;
    width: 25%;
    padding: 8px;
    line-height: 10px;
    font-size: 40px;

    h3{
      color: $textBigColor;
    }

.button{
    border-radius: 9px;
    padding: 8px;
    margin-bottom: 20px;
    margin-top: 10px;
    background-color: $buttonColor;
    color: $textColor;
  }
}

//   .active{
//         border-bottom:4px solid red;
//         color: $first_color;
//         padding-bottom: 20px;
//   }

</style>