<template>
  <section class="blog-one blog-page">
      <div class="container">
          <div class="row">
              <div class="col-lg-4" v-for="actu in news" :key="actu.id">
                  <div class="blog-one__single">
                      <div class="blog-one__image">
                          <img :src="
                  'https://app.cmabenin.bj/web/public/storage/' + actu.cover
                " alt="">
                          <nuxt-link class="blog-one__plus" :to="'/actus-details?post='+actu.id"><i class="kipso-icon-plus-symbol"></i>
                              <!-- /.kipso-icon-plus-symbol --></nuxt-link>
                      </div><!-- /.blog-one__image -->
                      <div class="blog-one__content text-center">
                          <div class="blog-one__meta">
                              <a data-toggle="tooltip" data-placement="top" title="" href="#" :data-original-title="formatDate(actu.created_at)"><i class="fa fa-calendar-alt"></i></a>
                              <a data-toggle="tooltip" data-placement="top" title="" href="#" :data-original-title=" actu.comments_count + 'Commentaire(s)'"><i class="fa fa-comments"></i></a>
                              <a data-toggle="tooltip" data-placement="top" title="" href="#" :data-original-title="'Post par' + actu.author"><i class="fa fa-user"></i></a>
                          </div><!-- /.blog-one__meta -->
                          <h2 class="blog-one__title"><nuxt-link  :to="'/actus-details?post='+actu.id">{{actu.title}}</nuxt-link>
                          </h2><!-- /.blog-one__title -->
                          <p class="blog-one__text">{{actu.content.substring(0, 100)}}</p><!-- /.blog-one__text -->
                          <nuxt-link :to="'/actus-details?post='+actu.id" class="blog-one__link">Lire plus</nuxt-link><!-- /.blog-one__link -->
                      </div><!-- /.blog-one__content -->
                  </div><!-- /.blog-one__single -->
              </div><!-- /.col-lg-4 -->
          </div><!-- /.row -->
          <!-- /.post-pagination -->
      </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
        name: "News",

        data() {
    return {
      news: []
    };
  },
  methods: {
    async getData() {
      // const apiLink = data.apiUrl.link;
      // apiLink+
      const res = await fetch("https://app.cmabenin.bj/api/posts");
      const finalRes = await res.json();
      this.news = finalRes.posts;
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
    // truncatedDescription( content) {
    //   if (content) {
    //     // Truncate the description to the first 100 characters
    //     return content.toString.substring(0, 100);
    //   }
    //   // If the description is empty, you can provide a default value or handle it accordingly
    //   return "No description available";
    // }
  }
    }
</script>

<style scoped>

</style>
