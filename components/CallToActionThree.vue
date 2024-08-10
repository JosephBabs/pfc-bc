<template>
  <section class="cta-three" id="beneficiaires">



    <div class="container  sf mt-sm-5">
      <div class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl" loading="lazy"
        style="background-image: url('/assets/images/slide/beneficiaires.jpeg');"><span
          class="mask bg-gradient-dark"></span>
        <div class="container">
          <div class="row" style="
    justify-content: center;">
            <div class="col-lg-6 ms-lg-5">
              <h4 class="text-white title">LES BÉNÉFICIAIRES DU PROJET</h4>

              <p class=" text-white desc"> <br />

                {{ truncatedText }}
                <span v-if="!isExpanded">{{ ellipsis }}</span>
              </p><a v-if="needsExpansion" type="button" href="#beneficiaires" class="text-white icon-move-right"
                @click="toggleText"> {{ buttonText }}</a>
            </div>
            <div class="image-container">
              <img src="/assets/images/slide/beneficiaires.jpg" alt="" />
            </div>
          </div>
        </div>
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
      truncateLength: 750, // Adjust this value based on your design
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
:root {
  --font-family-primary: "Vollkorn", serif;
  --font-family-secondary: "PT Sans", sans-serif;

  --font-size-title: 32px;
  --line-height-title: 1.4;
  --font-size-caption: 14px;
  --line-height-caption: 1.2;

  --color-text: #222022;
  --color-highlight-primary: #ffef7e;
  --color-highlight-secondary: #b7f9e9;
  --border-radius-primary: 32px;
}

.page-header {
  padding: 0;
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  background-size: cover;
  background-position: 50%;
}

@media (min-width: 768px) {
  .py-md-5 {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }


}

.border-radius-xl {
  border-radius: .75rem;
}

.mask {
  position: absolute;
  background-size: cover;
  background-position: center center;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: .8;
}

.container {
  --bs-gutter-x: 1.5rem;
  --bs-gutter-y: 0;
  width: 100%;
  padding-right: calc(var(--bs-gutter-x)* 1);
  padding-left: calc(var(--bs-gutter-x)* 1);
  margin-right: auto;
  margin-left: auto;
}

.sf {
  width: 100%;
}

.bg-gradient-dark {
  background-image: linear-gradient(195deg, #42424a 0%, #191919 100%);
}

.page-header .container {
  z-index: 1;
}

.title {
  font-size: 22px;
}

@media (min-width: 1200px) {

  .container-xl,
  .container-lg,
  .container-md,
  .container-sm,
  .container {
    max-width: 100%;
    width: 100%;
  }

  .title {
    font-size: 40px;
    font-weight: 900;
  }

  .desc {
    font-size: 20px;
  }
}

@media (min-width: 992px) {

  .container-lg,
  .container-md,
  .container-sm,
  .container {
    max-width: 100%;
  }

  .title {
    font-size: 40px;
    font-weight: 900;
  }

  .desc {
    font-size: 20px;
  }
}

@media (min-width: 768px) {

  .container-md,
  .container-sm,
  .container {
    max-width: 100%;
  }

  .title {
    font-size: 30px;
    font-weight: 900;
  }

  .desc {
    font-size: 15px;
  }
}

@media (min-width: 576px) {

  .container-sm,
  .container {
    max-width: 100%;
  }

  .title {
    font-size: 40px;
    font-weight: 900;
  }

  .desc {
    font-size: 20px;
  }

}


body {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  padding: 0;
  margin: 0;
}

* {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

@mixin mediaBig {
  @media (min-width: 576px) {
    @content;
  }
}

@include mediaBig {
  :root {
    --font-size-title: 40px;
  }
}

.card {
  max-width: 960px;
  border-radius: var(--border-radius-primary);
  box-shadow: 24px 24px 80px rgba(0, 0, 0, 0.1);
  padding: 20px 20px 28px 20px;
  box-sizing: border-box;
  margin: 20px;
  display: flex;
  flex-direction: column;

  @include mediaBig {
    flex-direction: row;
    align-items: center;
    margin: 40px;
    padding: 32px;
  }
}

.card__image {
  width: 100%;
  max-height: 300px;
  border-radius: var(--border-radius-primary);
  object-fit: cover;
  margin-bottom: 18px;

  @include mediaBig {
    width: 45%;
    max-height: none;
    min-height: 400px;
    margin-bottom: 0;
  }
}

.card__content {
  @include mediaBig {
    width: 55%;
    padding-left: 40px;
  }
}

.card__date {
  display: block;
  font-family: var(--font-family-secondary);
  font-size: var(--font-size-caption);
  line-height: var(--line-height-caption);
  text-transform: uppercase;
  color: var(--color-text);
  margin-bottom: 6px;

  @include mediaBig {
    margin-bottom: 8px;
  }
}

.card__title {
  font-family: var(--font-family-primary);
  font-size: var(--font-size-title);
  line-height: var(--line-height-title);
  color: var(--color-text);
  box-decoration-break: clone;
  background-image: linear-gradient(90deg,
      var(--color-highlight-primary),
      var(--color-highlight-secondary));
  background-size: 100% 42%;
  background-repeat: no-repeat;
  background-position: 0 85%;
  padding: 0 4px;
  margin-left: -4px;
}


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
    margin-bottom: 20px;
    /* Space between image and text */
    max-width: 100%;
  }

  .text-container {
    max-width: 100%;
  }
}
</style>
