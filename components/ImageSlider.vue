<template>
    <div class="slider">
        <div class="slides">
            <div v-for="(image, index) in images" :key="index"
                :class="{ 'slide': true, 'active': index === currentIndex }">
                <img :src="image.src" class="overImg" :alt="image.alt">
                <h1 class="overText">{{ image.overlayText }}</h1>
            </div>
        </div>
        <div class="prev" @click="moveSlide(-1)">❮</div>
        <div class="next" @click="moveSlide(1)">❯</div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            images: [
                { src: "/assets/images/slide/slider1.jpg", alt: "Image 1", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider2.jpg", alt: "Image 2", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider3.jpg", alt: "Image 3", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider4.jpg", alt: "Image 4", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider5.jpg", alt: "Image 4", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider6.jpg", alt: "Image 4", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider7.jpg", alt: "Image 4", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider8.jpg", alt: "Image 4", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider9.jpg", alt: "Image 4", overlayText: "Projet Forêts Classées du Bénin" }
            ],
            currentIndex: 0,
            intervalId: null
        };
    },
    mounted() {
        this.startSlideshow();
    },
    methods: {
        moveSlide(n) {
            clearInterval(this.intervalId); // Clear interval when manually moving slide
            this.currentIndex += n;
            if (this.currentIndex >= this.images.length) {
                this.currentIndex = 0;
            }
            if (this.currentIndex < 0) {
                this.currentIndex = this.images.length - 1;
            }
            this.startSlideshow(); // Restart slideshow after manual movement
        },
        startSlideshow() {
            this.intervalId = setInterval(() => {
                this.currentIndex++;
                if (this.currentIndex >= this.images.length) {
                    this.currentIndex = 0;
                }
            }, 5000); // Change slide every 5 seconds
        }
    }
};
</script>

<style scoped>
.slider {
    position: relative;
    width: 100%;
    /* max-width: 800px; Adjust as needed */
    margin: 0 auto;
    overflow: hidden;
}

.slides {
    display: flex;
    transition: opacity 1s ease-in-out;
}

.slide {
    width: 100%;
    opacity: 0;
    position: absolute;
    left: 0;
    top: 0;
}
@media only screen and (max-width: 768px){
    .slider {
    position: relative;
    width: 100%;
    height: 100%;
    /* max-width: 800px; Adjust as needed */
    margin: 0 auto;
    overflow: hidden;
}
.overImg {
    width: 100%;
    height: 100%;
    object-fit: contain; 
}
.overText {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 2rem; 
    z-index: 1;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
} 
.slides {
    display: flex;
    transition: opacity 1s ease-in-out;
}

.slide {
    width: 100%;
    opacity: 0;
    position: absolute;
    left: 0;
    top: 0;
}

}

.slide.active {
    opacity: 1;
}

img {
    width: 100%;
    height: auto;
}

h1 {
    position: absolute;
    top: 35%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 4rem; 
    z-index: 1;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
} 

.prev,
.next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    cursor: pointer;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    z-index: 2;
}

.prev {
    left: 0;
}

.next {
    right: 0;
}
</style>