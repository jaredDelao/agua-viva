<template>
    <div class="slider">
        <div class="title">
            <p>¿Que nos hace ser lo que somos?</p>
        </div>
        <carousel :autoplay="autoplayInterval" :items-to-show="1.9" :breakpoints="breakpoints" :wrap-around="true"
            @slide-start="changeSlide">
            <slide v-for="(slide, index) in slides" :key="index">
                <div class="slide-content">
                    <span class="xlg" :style="{ fontSize: index === currentIndex ? '6em' : '3em' }">{{ slide }}</span>
                    <span class="lg" :style="{ fontSize: index === currentIndex ? '4em' : '2em' }">{{ slide }}</span>
                    <span class="md" :style="{ fontSize: index === currentIndex ? '3em' : '1.5em' }">{{ slide }}</span>
                    <span class="xs" :style="{ fontSize: index === currentIndex ? '2.3em' : '1em' }">{{ slide }}</span>
                </div>
            </slide>
        </carousel>
        <div class="btn">
            <button type="button">
                Únete a nuestra comunidad
            </button>
        </div>
    </div>
</template>

<script>
import { Carousel, Slide } from "vue3-carousel";
import 'vue3-carousel/dist/carousel.css'

export default {
    name: 'Slider',
    components: {
        Carousel, Slide
    },
    data() {
        return {
            slides: ["Tolerancia", "Comprensión", "Respeto"],
            autoplay: true,
            autoplayInterval: 3000,
            currentIndex: 0,
            breakpoints: {
                // 700px and up
                576: {
                    itemsToShow: 2.2,
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
    background: #FFA219;
    padding-top: 200px;
    padding-bottom: 200px;
}

.slider .title {
    text-align: center;
    font-size: 30px;
    color: #fff;
    margin-bottom: 30px;
    line-height: 1.2em;
}

.slider .title p {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    padding-right: 20px;
    padding-left: 20px;
}

.slider .btn {
    text-align: center;
    margin-top: 50px;
}

.slider .btn button {
    outline: none;
    background: #fff;
    color: black;
    padding: 20px 35px;
    font-size: 16px;
    font-weight: 700;
    border-radius: 50px;
    border: none;
    margin: auto;
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
    min-height: 100px;
}

.slide-content span {
    transition: all 0.1s ease-in-out;
}

.slide-content .xs .slide-content .md,
.slide-content .xlg .slide-content .lg {
    display: none;
}

@media screen and (min-width: 0px) {
    .slide-content .xs {
        display: block;
    }

    .slide-content .md,
    .slide-content .xlg,
    .slide-content .lg {
        display: none;
    }
}

@media screen and (min-width: 576px) {
    .slide-content .md {
        display: block;
    }

    .slide-content .xs,
    .slide-content .xlg,
    .slide-content .lg {
        display: none;
    }
}

@media screen and (max-width: 576px) {
    .slider .title {
        font-size: 25px;
    }
}

@media screen and (min-width: 768px) {

    .slide-content .md,
    .slide-content .xlg,
    .slide-content .xs {
        display: none;
    }

    .slide-content .lg {
        display: block;
    }
}

@media screen and (min-width: 1200px) {

    .slide-content .xlg {
        display: block;
    }

    .slide-content .md,
    .slide-content .lg,
    .slide-content .xs {
        display: none;
    }
}
</style>