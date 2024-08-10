<template>
  <div>
    <div class="topbar-one">
      <div class="container">
        <div class="topbar-one__left">
          <!-- <a href="#">needhelp@kipso.com</a> -->
          <!-- (UIGP) – Projet Forêts Classées du Bénin
                                    Complexe CEN-SAD LAICO, Villa n°8 rue Steeve BIKO
                                    01 BP 3502 Cotonou <a href="#"> &nbsp; (+229) 99 99 06 08</a> -->
        </div>
        <!-- /.topbar-one__left -->
        <div class="topbar-one__right"></div>
        <!-- /.topbar-one__right -->
      </div>
      <!-- /.container -->
    </div>
    <!-- /.topbar-one -->
    <header class="site-header site-header__header-one">
      <nav class="navbar navbar-expand-lg navbar-light header-navigation stricky">


        <div class="container clearfix">
          <!-- Brand and toggle get grouped for better mobile display -->

          <div class="logo-box clearfix">
            <img src="/assets/images/logo-dark.png" alt="Logo 1" class="logo" />
            <img src="/assets/images/la-banque-mondiale-logo.png" alt="Logo 2" class="logo" />
          </div>
          <!-- /.header__social -->
          <button class="menu-toggler" data-target=".main-navigation">
            <span class="kipso-icon-menu"></span>
          </button>
          <!-- /.logo-box -->
          <!-- Collect the nav links, forms, and other content for toggling -->


          <div class="main-navigation">


            <ul class="navigation-box">
              <li :class="{ 'current': isActive('/') }">
                <nuxt-link to="/">Accueil</nuxt-link>
              </li>
              <li :class="{ 'current': isActive('/apropos') }">
                <nuxt-link to="/apropos">A propos</nuxt-link>
              </li>
              <li :class="{ 'current': isActive('/objectifs_et_indicateurs') }">
                <nuxt-link to="/objectifs_et_indicateurs">Objectifs et indicateurs</nuxt-link>
              </li>
              <li :class="{ 'current': isActive('/composantes') }">
                <nuxt-link to="/composantes">Composantes</nuxt-link>
              </li>
              <li :class="{ 'current': isActive('/actus') }">
                <nuxt-link to="/actus">Actualités</nuxt-link>
              </li>
              <li :class="{ 'current': isActive('/documentheque') }">
                <nuxt-link to="/documentheque">Documenthèque</nuxt-link>
                <ul class="sub-menu">
                  <li><nuxt-link to="/documentheque#rapports">Rapports</nuxt-link></li>
                  <li><nuxt-link to="/documentheque#marchespublics">Marchés Publics</nuxt-link></li>
                  <li><nuxt-link to="/documentheque#autresdocs">Autres Documents</nuxt-link></li>
                </ul>
              </li>

              <li :class="{ 'current': isActive('/#beneficiaires' ?? '/contact' ) }">
                <nuxt-link to="#">Plus +</nuxt-link>
                <ul class="sub-menu">

                  <li>
                    <nuxt-link to="/#beneficiaires">Bénéficiaires</nuxt-link>
                  </li>
                  <li><a href="https://www.flickr.com/photos/201063064@N02/" target="_blank"
                      rel="noopener noreferrer">Galerie</a></li>
                  <li><nuxt-link to="/contact">Contact</nuxt-link></li>
                </ul>
              </li>
            </ul>
          </div>
          <!-- /.navbar-collapse -->
          <!-- /.right-side-box -->
        </div>
        <!-- /.container -->
      </nav>
      <div class="site-header__decor">
        <div class="site-header__decor-row">
          <div class="site-header__decor-single">
            <div class="site-header__decor-inner-1"></div>
            <!-- /.site-header__decor-inner -->
          </div>
          <!-- /.site-header__decor-single -->
          <div class="site-header__decor-single">
            <div class="site-header__decor-inner-2"></div>
            <!-- /.site-header__decor-inner -->
          </div>
          <!-- /.site-header__decor-single -->
          <div class="site-header__decor-single">
            <div class="site-header__decor-inner-3"></div>
            <!-- /.site-header__decor-inner -->
          </div>
          <!-- /.site-header__decor-single -->
        </div>
        <!-- /.site-header__decor-row -->
      </div>
      <!-- /.site-header__decor -->
    </header>
  </div>
</template>

<script>
export default {
  name: "NavOne",
  methods: {
    isActive(routePath) {
      return this.$route.path === routePath;
    }
  },
  mounted() {
    if ($(".main-navigation .navigation-box").length) {
      var subMenu = $(".main-navigation .sub-menu");
      subMenu
        .parent("li")
        .children("a")
        .append(function () {
          return '<button class="sub-nav-toggler"> <span class="sr-only">Toggle navigation</span> <span class="icon-bar"></span> <span class="icon-bar"></span> <span class="icon-bar"></span> </button>';
        });
      var mainNavToggler = $(".header-navigation .menu-toggler");
      var subNavToggler = $(".main-navigation .sub-nav-toggler");
      mainNavToggler.on("click", function () {
        //alert()
        var Self = $(this);
        var menu = Self.data("target");
        $(menu).slideToggle();
        $(menu).toggleClass("showen");
        return false;
      });
      subNavToggler.on("click", function () {
        var Self = $(this);
        Self.parent().parent().children(".sub-menu").slideToggle();
        return false;
      });
    }
  },
};
</script>
<style scoped>
.logo-container {
  display: flex;
  gap: 10px;
  /* Space between logos */
}

.showen{
  display: block; position: absolute; top: 90px;

}

.logo {
  width: 150px;
  /* Set a fixed width for logos */
  height: auto;
  /* Maintain aspect ratio */
  max-width: 100%;
  /* Ensure logos do not overflow */
  object-fit: contain;
  /* Ensure logos fit well */
}

/* Mobile Styles */
@media (max-width: 768px) {

  .logo {
    width: 90px;
    /* Set a fixed width for logos */
    height: auto;
    /* Maintain aspect ratio */
    max-width: 100%;
    /* Ensure logos do not overflow */
    object-fit: contain;
    /* Ensure logos fit well */
    margin-bottom: -70px;
    padding-top: 10px
  }
}
</style>