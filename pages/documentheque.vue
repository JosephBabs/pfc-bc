<template>
    <div>
      <NavOne />
      <PageHeader title="Documenthèque (PFC Bénin)" />
      
      
      
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
    import PageHeader from "../components/PageHeader";
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
        PageHeader,
        Autredocs,
        NavOne,
        Footer,
      }
    }
  </script>
  