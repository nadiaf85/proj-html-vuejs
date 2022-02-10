<template>

<section class="popular_dishes">
    <div class="delivery">
        <span><i class="far fa-clock"></i> 24/7 Delivery</span>
        <span><i class="fas fa-hamburger"></i> Over 100 Dishes</span>
        <span><i class="fas fa-mobile-alt"></i> In App Ordering</span>
        <span><i class="fas fa-car"></i> Fast Delivery</span>
    </div>
    <h1>Our Most Popular Dishes</h1>
    <div class="container">
        <div class="dishes">
            <div v-for="(element,index) in dishesType" :key="index">
                <img :src="element.image" alt="">
                <div class="view_cart">
                    <p class="check"><i class="far fa-check-square"></i></p>
                    <p class="view">View cart</p>
                </div>
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
    position: relative;

    &:hover .view_cart{
        display: block;
    }

    .check{
        font-size: 30px;
        border: 3px solid black;
        padding: 10px;
        border-radius: 40px;
        background-color: black;
        color: $textColor;
        height: 57px;
        transform: translate(174px, -326px);
        width: 72%;
    }

    .view{
        font-size: 13px;
        color: $textColor;
        transform: translate(164px, -326px);
        text-transform: uppercase;
        font-weight: bold;
    }

    img{
        padding: 10px;

        &:hover {
            filter: brightness(75%);
        }
    }

    p{
        text-align: center;
        line-height: 30px;
    }
}

.view_cart{
    position: absolute;
    display: none;

    &:hover .dishes{
        display: block;
    }
}

.type{
    font-size: 25px;
}

.price{
    color: $buttonColor;
    font-weight: 200;
    font-size: 14px;
}

.button{
    display: flex;
    justify-content: center;
    margin-top: 30px;

    button{
        border: 1px solid $buttonColor;
        border-radius: 20px;
        padding: 8px;
        margin-bottom: 70px;
        margin-top: 10px;
        background-color: $buttonColor;
        color: $textColor;
        text-transform: uppercase;
        width: 16%;
        font-weight: bold;
    }
}

.delivery{
    text-align: center;
    height: 50px;
    font-size: 17px;

    span{
        padding: 35px;
        text-transform: uppercase;
        background-color: $textColor;
    }
}

</style>