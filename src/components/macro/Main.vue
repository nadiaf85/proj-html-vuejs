<template>

<section>
    
    <MainDishes/>
    <MainBannerDiscount/>
    <MainMenuCategories/>
    <MainBannerDownload/>
    <MainLatestNews/>
    
</section>

  
</template>

<script>
import MainDishes from '../sections/MainDishes.vue'
import MainBannerDiscount from '../sections/MainBannerDiscount.vue'
import MainMenuCategories from '../sections/MainMenuCategories.vue'
import MainBannerDownload from '../sections/MainBannerDownload.vue'
import MainLatestNews from '../sections/MainLatestNews.vue'

export default {
    name: 'Main',
    components: {
        MainDishes,
        MainBannerDiscount,
        MainMenuCategories,
        MainBannerDownload,
        MainLatestNews
    },
}

</script>

<style lang="scss" scoped>



</style>