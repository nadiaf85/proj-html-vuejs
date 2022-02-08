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
                text: "Collectibles",
                url: "#",
                current: false,
            }
        ]
      }
  }
}
</script>

<style lang="scss" scoped>

header{
    height: 830px;
    background-image: url('../../assets/images/home-background-hero-scaled.jpg');
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
}

.container{
  display: flex;
  justify-content: space-between;
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
//   .active{
//         border-bottom:4px solid red;
//         color: $first_color;
//         padding-bottom: 20px;
//   }

</style>