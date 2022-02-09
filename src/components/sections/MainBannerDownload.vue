<template>
    <section class="banner_download">
        <div class="container_info">
            <div class="text_left">
                <p class="down">Download Our</p>
                <p class="app"><strong>Ordering App</strong></p>
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
@import '../../assets/style/vars.scss';

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
    width: 45%;
    padding: 8px;
    line-height: 50px;
    font-size: 76px;
}

.down{
    margin-top: 30px;
    font-size: 30px;
}

.app{
    color: $textBigColor;
}
</style>