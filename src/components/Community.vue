<template>
    <div class="slider">
        <div class="title">
            <p>Conoce a nuestra comunidad</p>
        </div>
        <carousel :autoplay="6000" :items-to-show="1.5" :breakpoints="breakpoints" :wrap-around="true"
            @slide-start="changeSlide" :transition="500">
            <slide :key="0">
                <img src="../assets/community/1.svg" alt="1"
                    :style="{ transform: 0 === currentIndex ? 'scale(1)' : 'scale(0.7)' }">
            </slide>
            <slide :key="1">
                <img src="../assets/community/2.svg" alt="2"
                    :style="{ transform: 1 === currentIndex ? 'scale(1)' : 'scale(0.7)' }">
            </slide>
            <slide :key="2">
                <img src="../assets/community/3.svg" alt="3"
                    :style="{ transform: 2 === currentIndex ? 'scale(1)' : 'scale(0.7)' }">
            </slide>
            <template #addons>
                <Pagination />
            </template>
        </carousel>
    </div>
</template>

<script>
import { Carousel, Slide, Pagination } from "vue3-carousel";
import 'vue3-carousel/dist/carousel.css'

export default {
    name: 'Community',
    components: {
        Carousel, Slide, Pagination
    },
    data() {
        return {
            slides: ["Tolerancia", "Comprensión", "Respeto"],
            autoplay: true,
            autoplayInterval: 3000,
            currentIndex: 0,
            breakpoints: {
                // 700px and up
                1100: {
                    itemsToShow: 1.9,
                },
            },
        }
    },
    methods: {
        changeSlide(event) {
            const indexTo = event.slidingToIndex;
            if (indexTo === 3) {
                this.currentIndex = 0;
                return;
            }
            this.currentIndex = indexTo;
        }
    }
}
</script>

<style scoped>
.slider {
    background: #fff;
    padding-top: 100px;
    padding-bottom: 100px;
}

.slider img {
    width: 100%;
    max-height: 600px;
    -webkit-box-shadow: 13px 13px 0px 0px rgba(255, 162, 25, 1);
    -moz-box-shadow: 13px 13px 0px 0px rgba(255, 162, 25, 1);
    box-shadow: 13px 13px 0px 0px rgba(255, 162, 25, 1);
    margin-bottom: 13px;
}

.slider .title {
    text-align: center;
    font-size: 30px;
    color: #000;
    margin-bottom: 40px;
}

.slider .title p {
    margin: 0;
    font-family: 'Poppins', sans-serif;
}


.slider .carousel {
    height: 100%;
}

.slide-content {
    width: 100%;
    text-align: center;
    height: 100%;
    color: #fff;
    font-weight: 700;
    vertical-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
}

.slide-content span {
    transition: all 0.1s ease-in-out;
}

.carousel__pagination {
    margin-top: 30px;
}
</style>