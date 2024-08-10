<!-- pages/index.vue -->
<template>
    <div>
      <div class="image-slider">
        <!-- Image slider component will be placed here -->
         <imageSlider/> 
      </div>
      <div class="content-overlay">
        <h1>Material Kit 2</h1>
        <p>Start the Development With Bootstrap 5 Design System inspired by Material Design.</p>
        <div class="stats">
          <div>
            <strong>70+</strong>
            <span>Coded Elements</span>
          </div>
          <div>
            <strong>15+</strong>
            <span>Design Blocks</span>
          </div>
          <div>
            <strong>4</strong>
            <span>Pages</span>
          </div>
        </div>
        <a href="#" class="btn btn-primary">FREE DOWNLOAD</a>
      </div>
    </div>
  </template>
  
<script>
    
  import ImageSlider from '~/components/imageSliders.vue';

  export default {
    components: {
      ImageSlider
    }
  }
</script>

  <style scoped>
  /* Add your CSS here */
  .image-slider {
  position: relative;
  width: 100%;
  height: 100vh; /* Full height */
  overflow: hidden;
}

.content-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: white;
}

.stats {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 20px 0;
}

.stats div {
  text-align: center;
}

.btn-primary {
  background-color: #007bff;
  border: none;
  padding: 10px 20px;
  color: white;
  text-transform: uppercase;
  text-decoration: none;
  cursor: pointer;
}

</style> 
  