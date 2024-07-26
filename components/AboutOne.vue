<template>
    <section class="about-one ">
        
        <div class="container text-center">
            <!-- /.block-title -->
            <div class="about-img" style="margin: 20px;">
                <div class="row">
                    <div class="col-lg-6">
                        <img src="/assets/images/about-2-1.jpeg" style="border-radius: 20px;" width="100%" height="auto" alt="">
                    </div><!-- /.col-lg-6 -->
                    <div class="col-lg-6">
                        <img src="/assets/images/about-1-1.jpeg" style="border-radius: 20px;" width="100%" height="auto"alt="">
                    </div><!-- /.col-lg-6 -->
                </div><!-- /.row -->
                
            </div>
        </div><!-- /.container -->

        <div class="collapsible-list">
            <div class="item">
                <div class="content">
                    <div class="block-title text-center">
                        <h3 class="block-title__title">PFC BENIN</h3>
                        <!-- /.block-title__title -->
                    </div>
                    <p> Le Projet Forêts Classées Bénin (PFC – B) contribue
                        au cadre de partenariat entre la Banque mondiale
                        et le Benin de 2018-2022 au travers de son (i)
                        Domaine d’intervention 1 «Transformation structurelle
                        par la compétitivité et la productivité», Objectif 3
                        «Améliorer la capacité de gouvernance pour l’efficacité
                        et la redevabilité», et (ii) Domaine d’intervention 3
                        «Accroître la résilience et les opportunités et réduire
                        la vulnérabilité liée au climat», objectif 8 «Faire face
                        aux menaces et aux vulnérabilités liées au climat».<br><br>
                        Le projet soutient ces objectifs en s’attaquant en
                        priorité à la faiblesse de la capacité opérationnelle de
                        l’Administration Forestière en établissant un cadre de
                        gouvernance opérationnelle plus solide pour assurer
                        une gestion efficace des FCs, associé à la mise en
                        œuvre de techniques d’intensification de l’agriculture,
                        de méthodes agroforestières visant à promouvoir
                        une agriculture résiliente au climat, et gestion des
                        ressources naturelles.<br><br> Le projet renforcera également
                        la protection des zones à haute valeur de conservation
                        et installera des plantations de bois de feu à grande
                        échelle pour répondre aux besoins énergétiques des
                        principales villes consommatrices (Cotonou, AbomeyCalavi et Porto-Novo).
                        
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "AboutOne"
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
