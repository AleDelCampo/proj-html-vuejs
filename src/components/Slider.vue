<script>
import Navbar from '../components/Navbar.vue';

export default {

    components: {
        Navbar,
    },

    data() {

        return {
            slides: [
                "src/assets/slider2-1.jpg",
                "src/assets/slider1-1.jpg",
                "src/assets/slider3.jpg",
                "src/assets/slider4.jpg"
            ],
            thisSlideIndex: 0
        };
    },

    methods: {
        
        prevSlide() {
            this.thisSlideIndex = (this.thisSlideIndex - 1 + this.slides.length) % this.slides.length;
        },
        
        nextSlide() {
            this.thisSlideIndex = (this.thisSlideIndex + 1) % this.slides.length;
        }
    },
};
</script>


<template>

   
    <div id="slider-container">

        <Navbar></Navbar>

        <img  
            v-for="(currentImage, index) in slides" 
            :src='currentImage' 
            v-show="index == thisSlideIndex"
            />
        <div @click="prevSlide()" class="prev"><i class="fa-solid fa-chevron-left"></i></div>
        <div @click="nextSlide()" class="next"><i class="fa-solid fa-chevron-right"></i></div>
    </div>

</template>


<style lang="scss" scoped>

#slider-container {
    position: relative;
    overflow: hidden;
    max-height: 910px;

    img {
        width: 100%;
        max-height: 910px;
    }
}

.prev, .next {
    position: absolute;
    top: 50%;
    border-radius: 50%;
    border: 2px white solid;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    font-size: 14px;
    padding: 14px 20px;
    z-index: 40;
    cursor: pointer;
}

.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.prev {
    left: 40px;
}

.next {
    right: 40px;
}
</style>