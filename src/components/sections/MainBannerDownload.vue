<template>
    <section class="banner_download">
        <div class="container_info">
            <div class="text_left">
                <p class="down">Download Our</p>
                <p class="app"><strong>Ordering App</strong></p>
                <span><img src="../../assets/images/app-store-badge-200x67.png" alt=""></span>
                <span><img src="../../assets/images/play-store-badge-200x67.png" alt=""></span>
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
    height: 425px;
    width: 100%;
}

.container_info{
    width: 80%;
    margin: auto;
}

.text_left{
    color: white;
    width: 45%;
    padding: 10px;
    line-height: 50px;
    font-size: 64px;

    span{
        margin-right: 10px;

        img{
            width: 35%;
        }
    }
}

.down{
    margin-top: 80px;
    font-size: 30px;
    line-height: 34px;
}

.app{
    color: $textBigColor;
    margin-bottom: 50px;
}
</style>