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
            {
                icon: "fa-solid fa-leafy-green",
            },
            {
                icon: "fa-solid fa-wheat-awn",
            },
            {
                icon: "fa-solid fa-wine-bottle",
            },
            {
                icon: "fa-solid fa-steak",
            }
        ]
      }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

.menu{
    margin-top: 90px;

    h1{
        text-align: left;
    }
}

.title_button{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 95%;
    margin-top: 40px;
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
    }
}

// .icon_type{
//     display: flex;
//     justify-content: center;
// }

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

</style>