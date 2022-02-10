<template>

<section class="container">
    <div class="news">
        <div class="title_button">
            <h1>Latest News</h1>
            <button type="button" class="button">Read more news <i class="fas fa-arrow-circle-right"></i></button>
        </div>
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
</section>

  
</template>

<script>
export default {
    name: 'MainLatestNews',
    data() {
      return{
        newType: [
            {
                image: require ("../../assets/images/pancake-burger.jpg"),
                title: "NEW: The Pancake Burger",
                description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex.Pellentesque commodo tortor vel mi",
            },
            {
                image: require ("../../assets/images/new-milkshake-menu.jpg"),
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
    margin-top: 80px;
    margin-bottom: 80px;

    h1{
        text-align: left;
        font-size: 30px;
        margin-top: 50px;
        margin-bottom: 50px;
    }
}

.title_button{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 95%;
}

.new_type{
    display: flex;
    justify-content: center;

    img{
        padding: 2px;
        width: 90%;

        &:hover {
            filter: brightness(75%);
        }
    }

    p{
        text-align: center;
        line-height: 10px;
    }
}

.text_news{
    width: 94%;

    p{
        line-height: 20px;
    }

    .type{
        font-size: 25px;
        margin-bottom: 20px;
        margin-top: 20px;
    }

    .information_type{
        font-size: 15px;
        width: 94%;
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
    width: 19%;
    font-weight: bold;
}


</style>