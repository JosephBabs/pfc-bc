<template>
    <div>
        <h2 class="blog-details__content-title">2 Comments</h2><!-- /.blog-details__content-title -->
                <div class="comment-one">
                    <div class="comment-one__single" v-for="comment in comments" :key="comment.id">
                        <div class="comment-one__image">
                            <div class="inner-block">
                                <img src="/assets/images/comment-1-1.jpg" alt="Awesome Image">
                            </div><!-- /.inner-block -->
                        </div><!-- /.comment-one__image -->
                        <div class="comment-one__content">
                            <div class="comment-one__content-top">
                                <div class="comment-one__top-left">
                                    <h3 class="comment-one__author">{{comment.fullname}}</h3>
                                    <!-- /.comment-one__author -->
                                    <p class="comment-one__date">{{ calcDate(comment.created_at) }}<span class="comment-one__date-sep">-</span> 4:00 pm</p>
                                    <!-- /.comment-one__date -->
                                    <p class="comment-one__text">{{comment.comment_description}}</p>
                                    <!-- /.comment-one__text -->
                                </div><!-- /.comment-one__top-left -->
                                <!-- /.comment-one__top-right -->
                            </div><!-- /.comment-one__content-top -->
                        </div><!-- /.comment-one__content -->
                    </div><!-- /.comment-one__single -->
                </div><!-- /.comment-one -->
                <h2 class="blog-details__content-title">Laissez un commentaire</h2><!-- /.blog-details__content-title -->
                <form  @submit.prevent="submitData" class="reply-form">
                    <div class="row">
                        <div class="col-lg-6">
                            <input type="text" placeholder="Votre nom" v-model="form.fullname" class="reply-form__field">
                        </div><!-- /.col-lg-6 -->
                        <div class="col-lg-6">
                            <input type="text"  placeholder="Email" v-model="form.email" class="reply-form__field">
                        </div><!-- /.col-lg-6 -->
                        <div class="col-lg-12">
                            <textarea v-model="form.comment_description" placeholder="Saisir le message" class="reply-form__field"></textarea>
                            <button class="reply-form__btn thm-btn" type="submit">Envoyer le Commentaire</button>
                        </div><!-- /.col-lg-12 -->
                    </div><!-- /.row -->
                </form>

                
    
      <div class="alert success-a" v-if="showAlert_s">
       Commentaire envoyé</div>

       <div class="alert danger-a" v-if="showAlert_d">
       Erreur: vérifiez votre connexion</div>
    </div>
</template>

<script>

// moment().format();
// const toasts = ;
 function showAlert(){
  setTimeout(() => {
    const elements = document.getElementsByClassName("alert");
    for (let i = 0; i < elements.length; i++) {
        elements[i].style.display = "none";
    }
}, 3000);

 }

async function postData(url, data) {
  try {
    const response = await fetch(url, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify(data),
    });

    if (!response.ok) {
      throw new Error('Network response was not ok');
      alert("Erreur de connexion")
    }

    const result = await response.json();
    return result;
  } catch (error) {
    console.error('Error:', error);
    throw error;
  }
};


  export default {
    
    name: "Comment",
    data() {
    return {
      comments: [],

      form: {
          
          fullname: "", 
          email: "",
          comment_description: "",
        },
      showAlert_s: false, // Initially, hide the alert
      showAlert_d: false, // Initially, hide the alert
      alertType: '',    // Type of the alert ('success' or 'error')
      alertMessage: '', // Message to display in the alert
    
    };
  },
  name: 'ContactForm',
    
  methods: {

    
      async getData() {
        const apiLink = dataT.apiUrl.link;
        const res = await fetch("https://app.cmabenin.bj/api/posts/"+this.$route.query.post);
        const finalRes = await res.json();
        // console.log(finalRes.post);
        // alert(apiLink + 'post/')
        this.comments = finalRes.comments;
      },
     calcDate(date) {
      let nowDate = moment();
      // let pickDate = moment(date.toString(), 'YYYY-MM-DD-SS');
      
    let dateDiff = moment.duration(nowDate.diff(date));
      
    switch (true) {
        case dateDiff.asSeconds() < 60:
            return "à l'instant";
        case dateDiff.asMinutes() < 60:
            return dateDiff.minutes() + ' min';
        case dateDiff.asHours() < 24:
            return dateDiff.hours() + ' hr(s)';
        case dateDiff.asDays() < 30:
            return dateDiff.days() + ' jr(s)';
        case dateDiff.asMonths() < 12:
            return dateDiff.months() + ' mois';
        default:
            return dateDiff.years() + ' an(s)';
    }

    
      },
   



      // skyned

      
      // Example usage in a component
  async  submitData() {
  const apiLink = dataT.apiUrl.link;
  const url = apiLink+'comments';
  const data = {
    
    post_id : this.$route.query.post,
    fullname: this.form.fullname, 
    email: this.form.email,
    comment_description: this.form.comment_description ,
          
  };

  try {
    const response = await postData(url, data);
    console.log('Response:', response);
    this.showAlert_s = true;
    //     this.alertType = 'success';
    //     this.alertMessage = 'Commentaire envoyé';
    
    this.comments.push(this.form)
    showAlert()
    
    // alert("Commentaire envoyé")

    
    // Handle the response data here
  } catch (error) {
    console.error('Error:', error);
    
    this.showAlert_d = true;
    
    showAlert()
    //     this.alertType = 'error';
    //     this.alertMessage = 'vérifiez votre connexion';
    // Handle errors here
  }
},
    },
    mounted() {
      this.getData()
      setInterval(this.getData(), 5000);
      const toasts = document.getElementById('toasts');
 
    }
    
  }
</script>



<style lang="scss" scoped>

</style>