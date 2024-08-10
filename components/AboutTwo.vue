<template>

  <section class="hero-section">
    

    <div class="container">
      <div class="row">
        
        <div class="col-lg-6 col-xl-6 card shadow miniz">
          <div class="about-content-style2">
            <div class="section-title" data-aos="fade-up" data-aos-duration="1000">

              <h2 class="title">Projet Forêts Classées du Bénin</h2>
              <p> Le Projet Forêts Classées Bénin (PFC BENIN) contribue au cadre de
              partenariat entre la Banque mondiale et le Benin de 2018-2022 au
              travers de son (i) Domaine d’intervention 1 «Transformation
              structurelle par la compétitivité et la productivité», ", Objectif
              3 «Améliorer la capacité de gouvernance pour l’efficacité et la
              redevabilité», et (ii) Domaine d’intervention 3 «Accroître la
              résilience et les opportunités et réduire la vulnérabilité liée au
              climat», objectif 8 «Faire face aux menaces et aux vulnérabilités
              liées au climat» </p>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-xl-6" >
          <div class="right-image  card shadow">
            <img src="/assets/images/imageApropos.jpg" alt="Right Image" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutTwo",
};
</script>
<style scoped>
.hero-section {
  display: block;
  margin-top: -70px;
  /* height: 500px; Adjust based on your design */
  background-color: #fdfdfd;
  padding: 20px;
  background-size: cover;
  align-content: center;
}
.miniz{
  margin-right: -40px;
  z-index: 100;
}
.overlay {

  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to right, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0) 70%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  box-sizing: border-box;
}

.content {
  color: white;
  text-align: right;
}

.title {
  margin: 10px;
  font-size: 2.5rem;
  /* Adjust as needed */
}

.text {
  margin: 10px;
  font-size: 1.25rem;
  /* Adjust as needed */
}

.right-image img {
  width: 100%;
  /* Adjust as needed */
  height: auto;
  border-radius: 8px;
  /* Optional: add rounded corners */
}


/* Mobile Styles */
@media (max-width: 768px) {
  .overlay {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .title {
    margin: 10px;
    font-size: 2rem;
    font-weight: bolder;
    /* Adjust as needed */
  }

  .text {
    margin: 10px;
    font-size: 1.25rem;
    /* Adjust as needed */
  }

  .content {
    max-width: 90%;
    text-align: left;
    margin-bottom: 20px;
    /* Space between text and image */
  }

  .right-image {
    margin-top: 20px;
    margin-top: 20px;
    align-self: center;
    display: flex;
    align-content: flex-start;
    align-items: stretch;
    flex-wrap: nowrap;
    justify-content: space-around;
  }

  .right-image img {
    width: 100%;
    /* Ensure image fits within container */
    max-width: 100%;
    /* Maximum width for the image */
  }
}
</style>