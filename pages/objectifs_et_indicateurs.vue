<template>
<div>
    <NavOne />
    <PageHeader title="Objectifs et Indicateurs" />
    <CourseOne />
    <Footer />
  </div>
</template>
<script>
  import CourseOne from "../components/CourseOne";
  import PageHeader from "../components/PageHeader";
  import NavOne from "../components/NavOne";
  import Footer from "../components/Footer";
  export default {
    components: {Footer, NavOne, PageHeader, CourseOne},
    head(){
      return {
        title: "PFC BENIN | Objectifs et Indicateurs"
      }
    }
  }
</script>
