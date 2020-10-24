<template>
    <div v-swiper:mySwiper="swiperOption">
        <div class="banner-item">
        <h3 class="website_title">LEADERS IN ADVANCED CABLE INSTALLATION</h3>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            banners: [
                {
                    icon: 'man_with_screw.png',
                    url: '/'
                }
            ],
            swiperOption: {
                loop: true,
                speed: 1000,
                effect: 'fade',
                centeredSlides: true,
                autoplay: {
                    delay: 2500,
                    disableOnInteraction: true
                },
                pagination: {
                    el: '.swiper-pagination',
                    clickable: true
                }
            }
        }
    }
}
</script>

<style lang="scss">
.banner-item {
    height: 100vh;
    background-image: url('../../assets/img/wires.png');
    background-size: cover;
    cursor: pointer;
}

.website_title {
    font-size: 72px;
    text-align: center;
    padding-top: 18%;
    margin-left: 5%;
    margin-right: 5%;
    color: black;
}

.swiper-pagination-bullet-active {
    background: #ffffff;
}
</style>
