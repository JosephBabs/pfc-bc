
<template>
    <footer>
        <div class="footer-top">
            <div class="footer-container">
                <!-- A propos Column -->
                <div class="footer-column">
                    <h3>A propos</h3>
                    <p>Le Projet Forêts Classées Bénin (PFC BENIN)
                        contribue au cadre de partenariat entre la Banque mondiale et le
                        Benin de 2018-2022 au travers de son (i) Domaine d’intervention
                        1 «Transformation structurelle par la compétitivité et la productivité».</p>
                </div>

                <!-- Exploquer Column -->
                <div class="footer-column">
                    <h3>Explorer</h3>
                    <ul>
                        <li><nuxt-link to="/about">A propos </nuxt-link></li>
                        <li><nuxt-link to="/obj">Objectifs et indicateurs</nuxt-link></li>
                        <li><nuxt-link to="/composante">Composantes du PFC BENIN</nuxt-link></li>
                        <li><nuxt-link to="/beneficiaires">Bénéficiaires du PFC BENIN</nuxt-link></li>
                        <li><nuxt-link to="/gallery">Galerie</nuxt-link></li>
                        <li><nuxt-link to="/news">Actualités</nuxt-link></li>
                        <li> <nuxt-link to="/contact">Contact</nuxt-link></li>
                    </ul>
                </div>

                <!-- Contacts Column -->
                <div class="footer-column">
                    <h3>Contacts</h3>
                    <p>Unité Intégrée de Gestion des Projets (UIGP) – Projet Forêts Classées du Bénin
                                    Complexe CEN-SAD LAICO, Villa n°8 rue Steeve BIKO
                                    01 BP 3502 Cotonou</p>
                    <p><strong>Téléphone:</strong> <a href="tel:+22999990608"> (+229) 99 99 06 08</a></p>
                    <!-- <p><strong>Email:</strong><a href="mailto:contact@pfc.uigp.com"> contact@pfc.uigp.com</a></p> -->
                    <p><strong>Site Web:</strong> <a href="https://cadredevie.gouv.bj/" target="_blank"> www.cadredevie.gouv.bj/</a></p>
                </div>
            </div>
        </div>

        <!-- Footer Bottom -->
        <div class="footer-bottom">
            <p>&copy; {{ currentYear }}</p> 
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterComponent',

    data() {
        return {
            currentYear: new Date().getFullYear()
        };
    }
};
</script>


</script>

<style scoped>
footer {
  color: #fff;
}

.footer-top {
  background-color: #076d46;
  padding: 20px 0;
}

.footer-container {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.footer-column {
  flex: 1;
  min-width: 200px;
  margin: 0 10px;
}

.footer-column h3 {
  margin-top: 0;
  font-size: 1.25rem;
  font-weight: 900
}

.footer-column a {
  margin-top: 0;
  font-size: 1.25rem;
  /* font-weight: 900; */
  color:#ffffff;
}



.footer-column ul {
  list-style-type: none;
  padding: 0;
}

.footer-column ul li {
  margin: 10px 0;
}

.footer-column ul li a {
  color: #fff;
  text-decoration: none;
}

.footer-column ul li a:hover {
  text-decoration: underline;
}

.footer-bottom {
  background-color: #004d30; /* Darker color for the bottom section */
  text-align: center;
  padding: 10px 0;
}
</style>
