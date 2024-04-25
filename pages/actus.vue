<template>
  <div>
    <NavOne />
    <PageHeader title="Actualités" />
    <News />
    <Footer />
  </div>
</template>
<script>
  import PageHeader from "../components/PageHeader";
  import NavOne from "../components/NavOne";
  import Footer from "../components/Footer";
  import News from "../components/News";
  export default {
    components: {Footer, NavOne, PageHeader, News},
    head(){
      return {
        title: "PFC BENIN | Actualités"
      }
    }
  }
</script>
