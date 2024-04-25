<template>
    <div>
        <footer class="site-footer">
            <div class="site-footer__upper">
                <div class="container">
                    <div class="row">
                        <!-- /.col-lg-3 -->
                        
                        <div class="col-xl-3 col-lg-6 col-sm-12">
                            <div class="footer-widget footer-widget__link">
                                <h2 class="footer-widget__title">Explorer</h2><!-- /.footer-widget__title -->
                                <div class="footer-widget__link-wrap">
                                    <ul class="list-unstyled footer-widget__link-list">
                                        <li><nuxt-link to="/about">A propos </nuxt-link></li>
                                        <li><nuxt-link to="/obj">Objectifs et indicateurs</nuxt-link></li>
                                        <li><nuxt-link to="/composante">Composantes du PFC BENIN</nuxt-link></li>
                                        <li><nuxt-link to="/beneficiaires">Bénéficiaires du PFC BENIN</nuxt-link></li>

                                        <li><nuxt-link to="/gallery">Galerie</nuxt-link></li>


                                        <li>
                                            <nuxt-link to="/news">Actualités</nuxt-link>
                                        </li>
                                        <li>
                                            <nuxt-link to="/contact">Contact</nuxt-link>
                                        </li>
                                        <br>
                                        <br>
                                    </ul><!-- /.footer-widget__link-list -->
                                    <!-- /.footer-widget__link-list -->
                                </div><!-- /.footer-widget__link-wrap -->
                            </div><!-- /.footer-widget -->
                        </div><!-- /.col-lg-3 -->
                        <div class="col-xl-5 col-lg-6 col-sm-12">
                            <div class="footer-widget footer-widget__about">
                                <h2 class="footer-widget__title">A propos</h2><!-- /.footer-widget__title -->
                                <p class="footer-widget__text">Le Projet Forêts Classées Bénin (PFC – B)
                                    contribue au cadre de partenariat entre la Banque mondiale et le
                                    Benin de 2018-2022 au travers de son (i) Domaine d’intervention
                                    1 «Transformation structurelle par la compétitivité et la productivité»,
                                </p><!-- /.footer-widget__text -->
                                <!-- /.footer-widget__btn-block -->
                            </div><!-- /.footer-widget -->
                        </div>
                        <!-- /.col-lg-3 -->
                        <div class="col-xl-4 col-lg-6 col-sm-12">
                            <div class="footer-widget footer-widget__about">
                                <h2 class="footer-widget__title">Contacts</h2><!-- /.footer-widget__title -->
                                <p class="footer-widget__text">
                                    Unité Intégrée de Gestion des Projets (UIGP) – Projet Forêts Classées du Bénin
                                    Complexe CEN-SAD LAICO, Villa n°8 rue Steeve BIKO
                                    01 BP 3502 Cotonou -</p>
                                <ul class="list-unstyled footer-widget__link-list">
                                    <li><a href="tel:+22999990608">Tél : (+229) 99 99 06 08</a></li>
                                    <li><a href="https://cadredevie.gouv.bj/" target="_blank">www.cadredevie.gouv.bj/</a>
                                    </li>
                                </ul>
<!-- /.footer-widget__text -->
                                <!-- /.footer-widget__btn-block -->
                            </div><!-- /.footer-widget -->
                        </div>

                        <!-- /.col-lg-3 -->
                    </div>
                    

                    <form @submit.prevent="submitDat">

                        <div class="footer-widget__title">
                            <br>
                            <br>

                        </div>

                        <!-- <div class="footer_input-box">
                  <input type="email"
                    placeholder="E-mail"
                    name="email"
                    v-model="form.email"/>
                  <button type="submit" class="button"> 
                    <i class="fa fa-check"></i>
                  </button>
                </div> -->
                    </form><!-- /.row -->
                </div><!-- /.container -->
            </div><!-- /.site-footer__upper -->
            <div class="site-footer__bottom">
                <div class="container">
                    <p class="site-footer__copy">&copy; Copyright {{ new Date().getFullYear() }} <a
                            href="#"> </a> </p>
                    <div class="site-footer__social">

                    </div><!-- /.site-footer__social -->
                    <!-- /.site-footer__copy -->
                </div><!-- /.container -->
            </div><!-- /.site-footer__bottom -->
        </footer>

    </div>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped></style>
