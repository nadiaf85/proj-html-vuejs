<template>

<section class="popular_dishes">
    <h1>Our Most Popular Dishes</h1>
    <div class="container">
        <div class="dishes">
            <div v-for="(element,index) in dishesType" :key="index">
                <img :src="element.image" alt="">
                <p class="type"><strong>{{element.type}}</strong></p>
                <p class="price">{{element.price}}</p>
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
                image: require ("../../assets/images/skin-on-fries-400x571.jpg"),
                type: "Skin On Fries",
                price: "$ 3.00-$ 6.00",
            },
            {
                image: require ("../../assets/images/choco-cookie-frappe-400x571.jpg"),
                type: "Choco Cookie Frappe",
                price: "$ 4.99",
            },
            {
                image: require ("../../assets/images/donut-burger-400x571.jpg"),
                type: "The Donut Burger",
                price: "$ 6.99",
            }
        ]
      }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

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
        line-height: 30px;
    }
}

.type{
    font-size: 25px;
}

.price{
    color: $buttonColor;
    font-weight: 200;
}

.button{
    display: flex;
    justify-content: center;
    margin-top: 30px;

    button{
        border-radius: 20px;
        padding: 8px;
        margin-bottom: 20px;
        margin-top: 10px;
        background-color: $buttonColor;
        color: $textColor;
    }
    
}


</style>