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
                { src: "/assets/images/slide/slider5.jpeg", alt: "Image 5", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider6.jpeg", alt: "Image 6", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider7.jpeg", alt: "Image 7", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider8.jpeg", alt: "Image 8", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider9.jpeg", alt: "Image 9", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider10.jpeg", alt: "Image 10", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider11.jpeg", alt: "Image 11", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider12.jpeg", alt: "Image 12", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider13.jpeg", alt: "Image 13", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider15.jpeg", alt: "Image 14", overlayText: "Projet Forêts Classées du Bénin" },
                { src: "/assets/images/slide/slider16.jpeg", alt: "Image 15", overlayText: "Projet Forêts Classées du Bénin" },
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
    height: 80vh; /* Slider takes 60% of the viewport height */
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
    bottom: 0;
}

.slide.active {
    opacity: 1;
}

.overImg {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top center; /* Ensures images cover the slide area */
}

.overText {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 2rem; /* Adjusted for readability */
    z-index: 1;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.prev, .next {
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
    left: 10px;
}

.next {
    right: 10px;
}

/* Extra large screens */
@media (min-width: 1200px) {
    .overText {
        font-size: 3rem; /* Larger text on bigger screens */
    }
}

/* Mobile responsiveness */
@media (max-width: 768px) {
    .slider {
        height: 60vh; /* Maintains 60% height on mobile too */
    }

    .overText {
        font-size: 1.5rem; /* Smaller text on mobile devices */
    }
}
</style>
