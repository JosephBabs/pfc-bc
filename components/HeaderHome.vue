<template>
    <section class="inner-banner" style="">
      
      
    <ImageSlider />
      
    </section>
  </template>
  

  <script>
  import ImageSlider from '~/components/ImageSlider.vue';

      export default {
        name: "HeaderHome",
        props: {
          title: {
            type: String
          }
        },
        components: {
            ImageSlider
            }
      }
  </script>
  
  <style scoped>
  .slider {
    width: 100%;
    overflow: hidden;
    position: relative;
    height: 550px; 
  }
  .slides {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }
  .slide {
    width: 100%;
    flex-shrink: 0;
  }
  img {
    width: 100%;
    height: auto;
  }
  .prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    cursor: pointer;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    z-index: 1;
  }
  .prev {
    left: 0;
  }
  .next {
    right: 0;
  }
</style>
  