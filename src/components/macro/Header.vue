<template>
  <header>
      <div class="container">
            <div class="logo">
                <img src="../../assets/images/takeout-logo.png" alt="">
            </div>
            <nav>
                <ul v-for="(element, index) in info" :key="index">
                    <li>
                    <a href="#" :class="{'active': element.current==true}">{{element.text}}</a>
                    </li>
                    <li :class=(element.icon)></li>
                </ul>
            </nav>
        </div>
        <div class="container_info">
          <div class="text_left">
              <h5>Hungry?</h5>
              <h3>Great Food</h3>
              <p>Delivered</p>
              <button type="button" class="button">View our menu <i class="fas fa-arrow-circle-right"></i></button>
        </div>
      </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
      return{
        info: [
            {
                text: "Home",
                url: "#",
                current: true,
            },
            {
                text: "Order online",
                url: "#",
                current: false,
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
                icon: "fa-solid fa-cart-shopping",
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
  width: 100%;
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
     display: flex;
     align-items: baseline;

    ul{
    list-style-type: none;
    display: flex;
    justify-content: center;
    align-items: center;
    color: $textColor;
    padding: 8px;
    }

    li a{
      display: inline-block;
      color: $textColor;
      padding: 15px 10px;
      text-decoration: none;
      font-size: 12px;
      font-weight: 600;
    }
  }

  .active{
      color: $textBigColor;
      padding-bottom: 20px;
  }

  .icon_cart{
    color: $textColor;
  }

.container_info{
    width: 80%;
    margin: auto;
}

.text_left{
    color: white;
    width: 45%;
    padding: 8px;
    line-height: 76px;
    font-size: 76px;
    margin-top: 120px;

    h3{
      color: $textBigColor;
    }

button{
    border: 1px solid $buttonColor;
    border-radius: 20px;
    padding: 8px;
    margin-bottom: 20px;
    margin-top: 10px;
    background-color: $buttonColor;
    color: $textColor;
    text-transform: uppercase;
  }
}

</style>