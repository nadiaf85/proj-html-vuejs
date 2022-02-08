<template>
    <section class="banner_download">
        <div class="container_info">
            <div class="text_left">
                <p>Download Our</p>
                <p>Ordering App</p>
            </div>
        </div>
</section>
</template>

<script>
export default {
    name: 'MainBannerDownload',
    
}
</script>

<style lang="scss" scoped>

.banner_download{
    background-image: url('../../assets/images/app-ordering-scaled.jpg') ;
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    height: 392px;
    width: 100%;
}

.container_info{
    width: 80%;
    margin: auto;
}

.text_left{
    color: white;
    width: 25%;
    padding: 8px;
}
</style>