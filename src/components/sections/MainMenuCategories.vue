<template>

<section class="menu">
    <h1>Menu Categories</h1>
    <button>View the full menu</button>
    <div class="container">
        <div class="categories">
            <div v-for="(element,index) in categoriesInfo" :key="index">
                <img :src="element.image" alt="">
            </div>
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
            },
            {
                image: require ("../../assets/images/burgers-menu-background.jpg"),
            },
            {
                image: require ("../../assets/images/pizza-menu-background.jpg"),
            },
            {
                image: require ("../../assets/images/fries-menu-background.jpg"),
            },
            {
                image: require ("../../assets/images/sides-menu-background.jpg"),
            },
            {
                image: require ("../../assets/images/desserts-menu-background.jpg"),
            },
            {
                image: require ("../../assets/images/beverages-menu-background.jpg"),
            },
            {
                image: require ("../../assets/images/specials-menu-background.jpg"),
            },
        ]
      }
  }
}
</script>

<style lang="scss" scoped>

.menu{
    margin-top: 90px;

    h1{
        text-align: left;
    }
}

.categories{
    margin: 2px;
    padding: 20px 13px;
    display: flex;
    flex-wrap: wrap;
    // width: 100%;
    justify-content: center;
    

    img{
        height: 241px;
        padding: 10px;
    }
}


</style>