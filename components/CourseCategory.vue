<template>
  <section class="thm-gray-bg course-category-one" id="composantes" >
    <div class="container-fluid text-center" style="">
      <div class="block-title text-center">
        <h2 class="block-title__title">Composantes du PFC BENIN</h2>
        <!-- /.block-title__title -->
      </div>
      <!-- /.block-title -->
      <div class="row">
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp">
            <div class="content">
              <h5>Appui à la Gouvernance du secteur</h5>
              <p>
                La première composante vise à renforcer la capacité de
                l’Administration forestière à améliorer la gestion du secteur et
                à mettre en place un instrument durable de financement à long
                terme des coûts récurrents de la gestion des forêts classées du
                pays
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-1.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp" data-wow-delay="300ms">
            <div class="content">
              <h5>Gestion Intégrée des Forêts Classées</h5>
              <p>
                L’objectif de cette composante est d’appuyer la gestion des FCs
                sélectionnées dans le sud (Dan, Dogo-Kétou, Logozohè, Toffo-Lama
                Sud) et dans le centre du pays (Agoua, Ouémé-Boukou et
                Tchaourou-Toui-Kilibo) de manière intégrée, à travers les quatre
                sous-composantes ci-dessous. dont les besoins en bois-énergie
                seront en partie satisfaits grâce aux interventions du projet.
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-2.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp" data-wow-delay="600ms">
            <div class="content">
              <h5>
                Développement de filières de Produits Forestiers Non Ligneux
                (PNFLs) sélectionnés
              </h5>
              <p>
                Traditionnellement, les communautés forestières exploitent les
                PFNLs à des fins domestiques, notamment nutritionnelles,
                médicales et cosmétiques. Les potentiels économiques des
                filières de ces produits ne sont perçus que partiellement et
                généralement sous-estimés. Les filières sont donc peu
                développées et leur valeur ajoutée est faible. En conséquence,
                les femmes, les hommes et les jeunes, trois segments de la
                population fortement impliqués dans la collecte et la
                transformation des PFNLs, en particulier la noix de karité
                (femmes) et le miel (hommes et jeunes), n’optimisent pas les
                revenus potentiels qu’offrent ces activités
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-3.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp" data-wow-delay="900ms">
            <div class="content">
              <h4>Gestion du projet</h4>
              <p>
                Cette composante appuiera l’administration quotidienne globale
                du projet, afin de garantir qu’un suivi et une évaluation
                réguliers sont effectués et que les résultats sont pris en
                compte dans la prise de décision relative à la mise en œuvre du
                projet.
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-4.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- /.course-category-one__carousel owl-carousel owl-theme --><!-- /.thm-btn -->
    </div>
    <!-- /.container-fluid -->
  </section>
</template>

<script>
export default {
  name: "CourseCategory",
};
</script>

<style scoped>
.service_1_single {
  background-color: #fff;
  border: #555555;
  padding: 2rem;
  box-shadow: inset #555555;
}
.service_1_single h3,
h4,
h5,
h6 {
  color: #140342;
  font-weight: 700;
  font-size: 20px;
}

#composantes{
    /* background-image: url(/assets/images/cta-bg-1-f.jpg); */
    background-repeat: no-repeat;
    background-size: cover;
    background-color: rgba(0, 255, 0, 0.2);
}

</style>
