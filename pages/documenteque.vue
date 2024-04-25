<template>
    <div>
      <NavOne />
      <!-- <BannerOne /> -->
      
      <!-- <HeaderHome title="Documentèque (PFC Bénin)" /> -->
      
      
      <Rapports />
      <Marches />
      <Autredocs />
      <Footer />
    </div>
  </template>
  
  <script>
  
    // import ImageSlider from '~/components/ImageSlider.vue';
  
    import NavOne from "../components/NavOne";
    import BannerOne from "../components/BannerOne";
    import HeaderHome from "../components/HeaderHome";
    import Footer from "../components/Footer";
    import Rapports  from "../components/Rapports"; 
    import Marches  from "../components/Marches"; 
    import Autredocs  from "../components/autresdocs"; 
    //Autredocs
  
    export default {
      components: {
        HeaderHome,
        BannerOne,
        Rapports,
        Marches,
        Autredocs,
        NavOne,
        Footer,
      }
    }
  </script>
  