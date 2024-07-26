<template>
  <section class="blog-details">
    <div class="single-post">
    <div class="post-header">
      <img :src="'https://uigp.bj/portal/public/storage/' +news.cover" alt="Cover Image" v-if="news.cover" class="cover-image" />
      <h1>{{ news.title }}</h1>
      <p class="post-meta">{{ formatDate(news.created_at) }}</p>
    </div>
    <div class="post-content" v-html="news.content"></div>
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
      // const apiLink = dataT.apiUrl.link;

      const res = await fetch(
        "https://uigp.bj/api/posts/" + this.$route.query.post
      );
      const finalRes = await res.json();
      // console.log(finalRes.post);
      // alert(finalRes)
      const post = finalRes.post; // Assuming post is an object with properties

      this.news = post;
      if (this.$route.query.post !== this.news.id) {
        const post = await fetchData(this.$route.query.post);
        this.news = post;
      }else{
        alert("error")
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
<style scoped>
.single-post {
  max-width: 90%;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.cover-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  margin-bottom: 20px;
}

.post-header {
  text-align: center;
  margin-bottom: 20px;
}

.post-header h1 {
  margin: 0;
  font-size: 2.5rem;
  font-weight: 700;
  color: #333;
}

.post-meta {
  color: #888;
  font-size: 0.875rem;
}

.post-content {
  font-size: 1.125rem;
  line-height: 1.6;
  color: #444;
}

.post-content p {
  margin-bottom: 1.5em;
}

@media (max-width: 768px) {
  
.post-header h1 {
  margin: 0;
  font-size: 1rem;
  font-weight: 700;
  color: #333;
}

.post-content {
  font-size: .925rem;
  line-height: 1.6;
  color: #444;
}
}
</style>