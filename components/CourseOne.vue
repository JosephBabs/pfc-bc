<template>


    <section class="thm-gray-bg course-category-one overlay " id="objectives-de-la-pcb">

        <div class="bgh">
            <div class="collapsible-list">
                <div class="item">
                    <div class="content">
                        <div class="block-title text-center">
                            <h3 class="block- title">Amélioratoin de la Gestion Durable des Forêts et Promotion des Chaînes de <br> valeur pour le Dévéloppement Communaire 
                                </h3>
                            <!-- /.block-title__title -->
                        </div>
                        <div class="row">
                            <div class="col-lg-6">
                                <p>
                                    L’Objectif de Développement du Projet est
                            d’améliorer la gestion intégrée des Forêts Classées
                            ciblées, de faciliter l’accès des principaux centres de
                            consommation au bois-énergie produit de manière
                            durable, et de promouvoir la chaîne des valeurs de
                            PFNL ciblés améliorant les revenus des communautés
                            dépendantes des forêts.<br>
                            Il sera évalué sur la base d’indicateurs constitués entre
                            autres de :
                                </p>
                            </div>
                            <div class="col-lg-6">
                                <p> 
                        <ul>
                            <li>Superficie des forêts placées sous gestion durable
                                (ha) sur la base de critères définis ;</li>
                            <li>Emissions nettes de Gaz à Effet de Serre (GES)
                                (tCO2eq) ;</li>
                            <li>Volume sur pied de plantations de bois-énergie
                                (m3) ;</li>
                            <li>Communautés dépendantes des Forêts Classées
                                ciblées ayant un accès accru aux sources de revenus
                                à travers les chaînes de valeur des PFNL (ventilées
                                par sexe et par âge par PFNL ciblé) (nombre)</li>
                            <li>Satisfaction des bénéficiaires (niveau d’engagement
                                par genre et par âge dans chaque zone cible).</li>
                        </ul>
                        </p>
                            </div>

                        </div>
                        
                    </div>
                </div>
            </div>
        </div>

        <!-- /.container-fluid -->
    </section>

</template>

<script>
export default {
    name: "CourseOne"
}
</script>

<style scoped>

.overlay {
  
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background: linear-gradient(to right, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0) 70%); */
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  box-sizing: border-box;
}
.bgh {
    /* background-image: url(/assets/images/about-1-1.jpeg); */
}

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
</style>
