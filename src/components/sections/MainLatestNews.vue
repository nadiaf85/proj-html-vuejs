<template>

<section class="container">
    <div class="news">
        <h1>Latest News</h1>
        <button type="button">Start your order</button>
            <div class="new_type">
                <div v-for="(element,index) in newType" :key="index">
                    <img :src="element.image" alt="">
                    <div class="text_news">
                        <p class="type"><strong>{{element.title}}</strong></p>
                        <p class="information_type">{{element.description}}</p>
                    </div>
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
@import '../../assets/style/vars.scss';

.container{
    display: flex;
    justify-content: center;
}

.news{
    width: 60%;
    margin-top: 80px;
    margin-bottom: 80px;

    h1{
        text-align: left;
        font-size: 30px;
        margin-top: 50px;
        margin-bottom: 50px;
    }
}


.new_type{
    display: flex;
    justify-content: center;

    img{
        padding: 2px;
    }

    p{
        text-align: center;
        line-height: 10px;
    }
}

.text_news{
    width: 100%;

    p{
        line-height: 20px;
    }

    .type{
        font-size: 25px;
        margin-bottom: 20px;
        margin-top: 20px;
    }

    .information_type{
        font-size: 12px;
        width: 94%;
    }
}

.button{
    text-align: center;
    margin-bottom: 20px;
    margin-top: 10px;
    background-color: $buttonColor;
}


</style>