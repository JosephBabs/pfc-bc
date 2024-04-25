<template>
  <section class="blog-details">
    <div class="container">
      <div class="row">
        <div class="col-lg-8">
          <div class="blog-one__single">
            <div class="blog-one__image">
              <img
                :src="
                  'https://app.cmabenin.bj/web/public/storage/' + actu.cover
                "
                alt=""
              />
            </div>
            <!-- /.blog-one__image -->
            <div class="blog-one__content text-center">
              <div class="blog-one__meta">
                <a
                  data-toggle="tooltip"
                  data-placement="top"
                  title=""
                  href="#"
                  :data-original-title="formatDate(actu.created_at)"
                  ><i class="fa fa-calendar-alt"></i
                ></a>
                <a
                  data-toggle="tooltip"
                  data-placement="top"
                  title=""
                  href="#"
                  :data-original-title="actu.comments_count + 'Commentaire(s)'"
                  ><i class="fa fa-comments"></i
                ></a>
                <a
                  data-toggle="tooltip"
                  data-placement="top"
                  title=""
                  href="#"
                  :data-original-title="'Post par' + actu.author"
                  ><i class="fa fa-user"></i
                ></a>
              </div>
              <!-- /.blog-one__meta -->
              <h2 class="blog-one__title">{{ actu.title }}</h2>
              <!-- /.blog-one__title -->
              <p class="blog-one__text">
                Aelltes port lacus quis enim var sed efficitur turpis gilla sed
                sit
                {{ actu.content }}
              </p>
              <!-- /.blog-one__text --><!-- /.blog-one__text -->
            </div>
            <!-- /.blog-one__content -->
          </div>
          <!-- /.blog-one__single -->
          <div class="share-block">
            <!-- /.social-block -->
          </div>
          <!-- /.share-block -->
          <!-- /.blog-details__author -->
          <Comment />
          <!-- /.reply-form -->
        </div>
        <!-- /.col-lg-8 -->
        <!-- /.col-lg-4 -->
      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>
</template>

<script>
import Comment from "../components/comment";
export default {
  name: "NewsDetails",
  components: {
    Comment,
  },
  data() {
    return {
      news: {},
    };
  },
  methods: {
    reloadPage() {
      location.reload(); // Reload the page
    },

    async getData() {
      const apiLink = dataT.apiUrl.link;

      const res = await fetch(
        "https://app.cmabenin.bj/api/posts/" + this.$route.query.post
      );
      const finalRes = await res.json();
      // console.log(finalRes.post);
      const post = finalRes.post; // Assuming post is an object with properties

      this.news = post;
      if (this.$route.query.post !== this.news.id) {
        const post = await fetchData(this.$route.query.post);
        this.news = post;
      }
      // Display specific properties in the alert
      // alert("Post Title: " + post.title);
    },

    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    },
  },
  mounted() {
    this.getData();
    // Attach a click event listener to the <nuxt-link> element
    // const link = this.$el.querySelector('nuxt-link');
    // link.addEventListener('click', this.reloadPage); cma-B-nin-Web-main
  },
};
</script>

<style scoped></style>
