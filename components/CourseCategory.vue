<template>
  <section class="thm-gray-bg course-category-one" id="composantes" >
    

    <div class="collapsible-list">
      <div class="block-title text-center">
        <h2 class="block- title">Le PFC BENIN</h2>
        <!-- /.block-title__title -->
      </div>
    <div class="item" v-for="(item, index) in items" :key="index">
      <div class="title" @click="toggle(index)">
        
        <div class="row" style="justify-content: space-between; padding: 5px;">
          <div class="col-md-7"><h2>{{ item.title }}</h2></div>
          <div style="padding-right: 10px;"><span>
            <i :class="{'fas fa-chevron-down chevron': activeIndex !== index, 'fas fa-chevron-up chevron': activeIndex === index}"></i>
          </span></div>
        </div>
      </div>
      <div class="content" v-if="activeIndex === index">
        <p>{{ item.content }}</p>
      </div>
    </div>
  </div>

    <!-- /.container-fluid -->
  </section>
</template>

<script>
export default {
  name: "CourseCategory",
  data() {
    return {
      items: [
        { title: 'Appui à la Gouvernance du secteur', content: 'La première composante vise à renforcer la capacité de l’Administration forestière à améliorer la gestion du secteur et à mettre en place un instrument durable de financement à long terme des coûts récurrents de la gestion des forêts classées du pays.' },
        { title: 'Gestion Intégrée des Forêts Classées', content: 'L’objectif de cette composante est d’appuyer la gestion des FCs sélectionnées dans le sud (Dan, Dogo-Kétou, Logozohè, Toffo-Lama Sud) et dans le centre du pays (Agoua, Ouémé-Boukou et Tchaourou-Toui-Kilibo) de manière intégrée, à travers les quatre sous-composantes ci-dessous. dont les besoins en bois-énergie seront en partie satisfaits grâce aux interventions du projet' },
        { title: 'Développement de filières de Produits Forestiers Non Ligneux (PNFLs) sélectionnés', content: `Traditionnellement, les communautés forestières exploitent les PFNLs à des fins domestiques, notamment nutritionnelles, médicales et cosmétiques. Les potentiels économiques des filières de ces produits ne sont perçus que partiellement et généralement sous-estimés. Les filières sont donc peu développées et leur valeur ajoutée est faible. En conséquence, les femmes, les hommes et les jeunes, trois segments de la population fortement impliqués dans la collecte et la transformation des PFNLs, en particulier la noix de karité (femmes) et le miel (hommes et jeunes), n’optimisent pas les revenus potentiels qu’offrent ces activités.`},
        { title: 'Gestion du projet',  content: 'Traditionnellement, les communautés forestières exploitent les PFNLs à des fins domestiques, notamment nutritionnelles, médicales et cosmétiques. Les potentiels économiques des filières de ces produits ne sont perçus que partiellement et généralement sous-estimés. Les filières sont donc peu développées et leur valeur ajoutée est faible. En conséquence,' }
      ],
      activeIndex: null
    };
  },
  methods: {
    toggle(index) {
      this.activeIndex = this.activeIndex === index ? null : index;
    }
  }
};
</script>

<style scoped>
.collapsible-list {
  width: 100%;
  max-width: 90%;
  margin: 0 auto;
}

.item {
  border: 1px solid #ccc;
  border-radius: 8px;
  margin-bottom: 10px;
  overflow: hidden;
}

.title {
  background-color: #f9f9f9;
  padding: 15px;
  cursor: pointer;
}

.title h2 {
  margin: 0;
  font-size: 1.5rem;
  color: #333;
}

.content {
  padding: 15px;
  background-color: #fff;
}

.content p {
  margin: 0;
  font-size: 1rem;
  color: #666;
}


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
    text-align: center; /* Center text for mobile */
    position: relative;
  }

  .chevron {
    position: absolute;
    right: 40px; /* Adjust spacing as needed */
  }}
</style>
