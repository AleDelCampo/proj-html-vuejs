<script>
export default {

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

    <nav>
        <div id="slider-container">
            <img  
                v-for="(currentImage, index) in slides" 
                :src='currentImage' 
                v-show="index == thisSlideIndex"
                />
            <div @click="prevSlide()" class="prev"><i class="fa-solid fa-chevron-left"></i></div>
            <div @click="nextSlide()" class="next"><i class="fa-solid fa-chevron-right"></i></div>
        </div>
    </nav>

</template>


<style lang="scss">

#slider-container {
    position: relative;
    overflow: hidden;
    max-height: 800px;

    img {
        width: 100%;
        max-height: 800px;
    }
}

.prev, .next {
    position: absolute;
    top: 50%;
    border-radius: 50%;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    cursor: pointer;
    font-size: 14px;
    padding: 14px 20px;
    z-index: 1;
}

.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.prev {
    left: 34px;
}

.next {
    right: 34px;
}
</style>