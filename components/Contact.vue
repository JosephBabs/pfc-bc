<template>
    <div>
      <section class="contact-info-one">
          <div class="container">
              <div class="row">
                  <div class="col-lg-4">
                      <div class="contact-info-one__single wow fadeInDown animated" data-wow-duration="1500ms" style="visibility: visible; animation-duration: 1500ms; animation-name: fadeInDown;">
                          <div class="contact-info-one__icon"><i class="kipso-icon-manager"></i><!-- /.kipso-icon-manager -->
                          </div><!-- /.contact-info-one__icon -->
                          <h2 class="contact-info-one__title">A propos de nous </h2><!-- /.contact-info-one__title -->
                          <p class="contact-info-one__text">
                            Le Projet Forêts Classées Bénin (PFC – B) contribue au cadre de partenariat entre la Banque mondiale et le Benin de 2018-2022 au travers de son  Domaine
                             d’intervention 1 «Transformation structurelle par la compétitivité et la productivité»,
                          </p><!-- /.contact-info-one__text -->
                      </div><!-- /.contact-info-one__single -->
                  </div><!-- /.col-lg-4 -->
                  <div class="col-lg-4">
                      <div class="contact-info-one__single wow fadeInUp animated" data-wow-duration="1500ms" style="visibility: visible; animation-duration: 1500ms; animation-name: fadeInUp;">
                          <div class="contact-info-one__icon"><i class="kipso-icon-placeholder"></i>
                              <!-- /.kipso-icon-manager -->
                          </div><!-- /.contact-info-one__icon -->
                          <h2 class="contact-info-one__title">Adresse</h2><!-- /.contact-info-one__title -->
                          <p class="contact-info-one__text">Unité Intégrée de Gestion des Projets (UIGP) – 
                            Projet Forêts Classées du Bénin <br> Complexe CEN-SAD LAICO, Villa 
                            n°8 rue Steeve BIKO 01 BP 3502 Cotonou -
                            <br>
                            <br>
                            <br>
                        </p><!-- /.contact-info-one__text -->
                      </div><!-- /.contact-info-one__single -->
                  </div><!-- /.col-lg-4 -->
                  <div class="col-lg-4">
                      <div class="contact-info-one__single wow fadeInDown animated" data-wow-duration="1500ms" style="visibility: visible; animation-duration: 1500ms; animation-name: fadeInDown;">
                          <div class="contact-info-one__icon"><i class="kipso-icon-contact"></i><!-- /.kipso-icon-manager -->
                          </div><!-- /.contact-info-one__icon -->
                          <h2 class="contact-info-one__title">Contacts</h2><!-- /.contact-info-one__title -->
                          <p class="contact-info-one__text">
                            (+229) 99 99 06 08 <br> &nbsp; 
                            <br>
                            <br>
                            <br>
                            <br>
                            <br>
                        </p><!-- /.contact-info-one__text -->
                      </div><!-- /.contact-info-one__single -->
                  </div><!-- /.col-lg-4 -->
              </div><!-- /.row -->
          </div><!-- /.container -->
      </section>
<section class="contact-one">
          <div class="container">
              <h2 class="contact-one__title text-center">Prenez contact
                  </h2><!-- /.contact-one__title -->
              <form action="/assets/inc/sendemail.php" class="contact-one__form contact-form-validated" novalidate="novalidate">
                  <div class="row low-gutters">
                      <div class="col-lg-6">
                          <input type="text" name="name" placeholder="Nom et Prénom">
                      </div><!-- /.col-lg-6 -->
                      <div class="col-lg-6">
                          <input type="text" placeholder="Email" name="email">
                      </div><!-- /.col-lg-6 -->
                      <div class="col-lg-12">
                          <textarea placeholder="Saisissez votre message" name="message"></textarea>
                          <div class="text-center">
                              <button type="submit" class="contact-one__btn thm-btn">Envoyer</button>
                          </div><!-- /.text-center -->
                      </div><!-- /.col-lg-12 -->
                  </div><!-- /.row -->
              </form><!-- /.contact-one__form -->
              <div class="result text-center"></div><!-- /.result -->
          </div><!-- /.container -->
      </section>

      <iframe src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d3965.357161800984!2d2.3881194736650944!3d6.347777793642042!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2zNsKwMjAnNTIuMCJOIDLCsDIzJzI2LjUiRQ!5e0!3m2!1sfr!2sus!4v1721985687563!5m2!1sfr!2sus"  width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
</template>

<script>
    export default {
        name: "Contact"
    }
</script>

<style scoped>

</style>
