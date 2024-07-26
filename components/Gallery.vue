<template>
  <section class="gallery-one">
      <div class="container">
          <div class="row">
              <div class="col-lg-4 col-md-6" v-for="img in galerie" :key="img.id">
                  <div class="gallery-one__single">
                      <img :src="img.image" alt="">
                      <a :href="img.image" class="gallery-one__popup img-popup"><i class="kipso-icon-plus-symbol"></i><!-- /.kipso-icon-plus-symbol --></a>
                  </div><!-- /.gallery-one__single -->
              </div>
              
          </div><!-- /.row -->
      </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
        name: "Gallery",

        data() {
    return {
      galerie: []
    };
  },
  methods: {
    async getData() {
      // const apiLink = data.apiUrl.link;
      // apiLink+
      const res = await fetch("https://uigp.bj/api/galleries_project/2");
      const finalRes = await res.json();
      this.galerie = finalRes.galleries;
    },
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    }
  },
  mounted() {
    this.getData();
  },
  computed: {
    
  }
}
</script>
<style scoped>

</style>
