<template>
    <div class="banner_discount">
        <div class="custom-shape-divider-top-1644426629">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="shape-fill"></path>
            </svg>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MainBannerDiscount',
    
}
</script>

<style lang="scss" scoped>
.banner_discount{
    background-image: url('../../assets/images/first-order-background-scaled.jpg') ;
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    height: 392px;
    width: 100%;
    position: relative;
}

.custom-shape-divider-top-1644426629 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
}

.custom-shape-divider-top-1644426629 svg {
    position: relative;
    display: block;
    width: calc(102% + 1.3px);
    height: 198px;
    transform: rotateY(180deg);
}

.custom-shape-divider-top-1644426629 .shape-fill {
    fill: #FFFFFF;
}


</style>