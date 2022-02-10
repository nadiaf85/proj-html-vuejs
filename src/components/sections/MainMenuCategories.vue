<template>

<section class="container">
        <div class="title_button">
            <h1>Menu categories</h1>
            <button type="button" class="button">View the full menu <i class="fas fa-arrow-circle-right"></i></button>
        </div>
            <div class="categories">
                <div v-for="(element,index) in categoriesInfo" :key="index">
                    <img :src="element.image" alt="">
                </div>
            </div>

            <div class="type_categories">
                <div class="leaf">
                    <i class="fas fa-leaf" style="color:#228B22"></i>
                    <p>Vegetarian</p>
                </div>
                <div class="gluten">
                    <i class="fab fa-pagelines" style="color:#FFD700"></i> 
                    <p>Gluten Free</p>
                </div>
                <div class="bottle">
                    <i class="fas fa-wine-bottle" style="color:#6495ED"></i>
                    <p>Dairy Free</p>
                </div>
                <div class="steak">
                    <i class="fas fa-drumstick-bite" style="color:#A52A2A"></i>
                    <p>Keto Friendly</p>
                </div>
            </div>
</section>
  
</template>

<script>
export default {
    name: 'MainMenuCategories',
    data() {
      return{
        categoriesInfo: [
            {
                image: require ("../../assets/images/appetizers-menu-background.jpg"),
                text: "Appetizers"
            },
            {
                image: require ("../../assets/images/burgers-menu-background.jpg"),
                text: "Burgers"
            },
            {
                image: require ("../../assets/images/pizza-menu-background.jpg"),
                text: "Pizza"
            },
            {
                image: require ("../../assets/images/fries-menu-background.jpg"),
                text: "fries"
            },
            {
                image: require ("../../assets/images/sides-menu-background.jpg"),
                text: "Sides"
            },
            {
                image: require ("../../assets/images/desserts-menu-background.jpg"),
                text: "Desserts"
            },
            {
                image: require ("../../assets/images/beverages-menu-background.jpg"),
                text: "Beverages"
            },
            {
                image: require ("../../assets/images/specials-menu-background.jpg"),
                text: "Specials"
            },
        ]
      }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

.title_button{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 95%;
    margin-top: 60px;
    margin-left: 23px;

    h1{
        font-size: 30px;
    }
}

.categories{
    margin: 2px;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    justify-content: center;
    

    img{
        height: 241px;
        padding: 10px;
        filter: brightness(80%);
    }
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

.type_categories{
    width: 100%;
    font-size: 40px;
    display: flex;
    justify-content: space-around;
    margin-bottom: 50px;
    margin-top: 30px;
    text-align: center;

    p{
        font-size: 13px;
        margin-top: 5px;
        font-weight: bold;
    }
}
</style>