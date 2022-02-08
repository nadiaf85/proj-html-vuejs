<template>

<section class="news">
    <h1>Latest News</h1>
    <div class="container">
        <div class="new_type">
            <div v-for="(element,index) in newType" :key="index">
                <img :src="element.image" alt="">
                <p>{{element.title}}</p>
                <p>{{element.description}}</p>
            </div>
        </div>
    </div>
    
    <!-- <div class="button">
        <button type="button">Start your order</button>
    </div> -->
    
</section>

  
</template>

<script>
export default {
    name: 'MainLatestNews',
    data() {
      return{
        newType: [
            {
                image: require ("../../assets/images/pancake-burger-400x300.jpg"),
                title: "NEW: The Pancake Burger",
                description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex.Pellentesque commodo tortor vel mi",
            },
            {
                image: require ("../../assets/images/new-milkshake-menu-400x300.jpg"),
                title: "New Milkshake Menu",
                description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex.Pellentesque commodo tortor vel mi",
            },
        ]
      }
  }
}
</script>

<style lang="scss" scoped>
// @import '../../assets/style/variables.scss';

.container{
    display: flex;
    justify-content: center;
}

.news{
    h1{
        text-align: center;
    }
}


.new_type{
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