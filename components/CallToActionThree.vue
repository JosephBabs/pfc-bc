<template>
  <section class="cta-three" id="beneficiaires">
    
    <div class="row-container">
    <div class="image-container">
      <img src="/assets/images/cta-1.jpeg" alt="" />
    </div>
    <div class="text-container">
      <h1>LES BÉNÉFICIAIRES DU PROJET</h1>
      <p> <br />
              
              {{ truncatedText }}
              <span v-if="!isExpanded">{{ ellipsis }}</span>
            </p>
            <button v-if="needsExpansion" class="btn btn-primary" @click="toggleText">{{ buttonText }}</button>
    
              
    </div>
  </div>
    <!-- /.container -->
  </section>
</template>

<!-- <script>
export default {
  name: "CallToActionThree",
};
</script> -->

<script>
export default {
  name: 'CallToActionThree',
  data() {
    return {
      isExpanded: false,
      fullText: 'Les bénéficiaires directs du projet sont: (i) les communautés dépendantes des FCs ciblées par le projet, une population d’environ 536.368 habitants (68.954 ménages), dont 267.626 hommes et 268.204 femmes qui bénéficieront des revenus générés par les activités d’agroforesterie basées sur la performance, l’intensification agricole, ainsi que de la mise en œuvre du système taungya et le développement des chaînes de valeur des PFNL ciblés; et (ii) l’Administration Forestière dans son ensemble, dont les capacités seront renforcées pour améliorer la gouvernance forestière. Les bénéficiaires indirects sont des segments de la population de Cotonou, Abomey-Calavi et Porto-Novo, dont les besoins en bois-énergie seront en partie satisfaits grâce aux interventions du projet.',
      truncateLength: 250, // Adjust this value based on your design
    };
  },
  computed: {
    needsExpansion() {
      return this.fullText.length > this.truncateLength;
    },
    truncatedText() {
      return this.isExpanded ? this.fullText : this.fullText.substring(0, this.truncateLength);
    },
    ellipsis() {
      return this.needsExpansion && !this.isExpanded ? '...' : '';
    },
    buttonText() {
      return this.isExpanded ? 'Voir moins' : 'Voir plus';
    }
  },
  methods: {
    toggleText() {
      this.isExpanded = !this.isExpanded;
    }
  }
}
</script>

<style scoped>
.row-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #f9f9f9;
}

.image-container {
  flex: 1;
  max-width: 40%;
  margin-right: 20px;
}

.image-container img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.text-container {
  flex: 2;
  max-width: 60%;
}

.text-container h1 {
  margin-top: 0;
  font-size: 2rem;
  color: #333;
}

.text-container p {
  font-size: 1rem;
  color: #666;
}

/* Mobile Styles */
@media (max-width: 768px) {
  .row-container {
    flex-direction: column;
    align-items: center;
  }

  .image-container {
    margin-right: 0;
    margin-bottom: 20px; /* Space between image and text */
    max-width: 100%;
  }

  .text-container {
    max-width: 100%;
  }
}


</style>
