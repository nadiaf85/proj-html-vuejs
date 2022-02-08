<template>

<section class="popular_dishes">
    <h1>Our Most Popular Dishes</h1>
    <div class="container">
        <div class="dishes">
            <div v-for="(element,index) in dishesType" :key="index">
                <img :src="element.image" alt="">
                <p>{{element.type}}</p>
                <p>{{element.price}}</p>
            </div>
        </div>
    </div>
    
    <div class="button">
        <button type="button">Start your order <i class="fas fa-arrow-circle-right"></i></button>
    </div>
    
</section>

  
</template>

<script>
export default {
    name: 'Main',
    data() {
      return{
        dishesType: [
            {
                image: require ("../../assets/images/skin-on-fries-200x286.jpg"),
                type: "Skin On Fries",
                price: "$ 3.00-$ 6.00",
            },
            {
                image: require ("../../assets/images/choco-cookie-frappe-200x286.jpg"),
                type: "Choco Cookie Frappe",
                price: "$ 4.99",
            },
            {
                image: require ("../../assets/images/donut-burger-200x286.jpg"),
                type: "The Donut Burger",
                price: "$ 6.99",
            }
        ]
      }
  }
}
</script>

<style lang="scss" scoped>
// @import '../../assets/style/variables.scss';

.popular_dishes{
    h1{
        text-align: center;
        font-size: 30px;
        margin-top: 100px;
        margin-bottom: 50px;
    }
}

.dishes{
    display: flex;
    justify-content: center;

    img{
        padding: 10px;
    }

    p{
        text-align: center;
        line-height: 10px;
    }
}

.button{
    text-align: center;
    margin-bottom: 20px;
    margin-top: 10px;
    
    // background-color: $buttonColor;
}


</style>