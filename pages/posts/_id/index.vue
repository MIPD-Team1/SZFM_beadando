<template>
  <div class="single-post-page">
    <section class="post">
      <h1 class="post-title">{{loadedPost.title}}</h1>
      <div class="post-details">
        <div class="post-detail">Feltöltés dátuma: {{loadedPost.updatedDate |  date}}</div>
        <div class="post-detail">Eladó: {{loadedPost.author}}</div>
      </div>
      <div
        class="post-thumbnail"
        :style="{backgroundImage: 'url(' + loadedPost.thumbnail + ')'}"></div>
      <p class="post-content">Leírás:<br> </br>{{loadedPost.content}}</p>

      <p class="post-previewText">{{loadedPost.previewText}}</p>
    
    </section>
    <section class="post-feedback">
      <p>Elérhetőség email cím <a href="mailto:feedback@my-awesome-domain.com">TeBoltod@info.com</a>.</p>
    </section>
  </div>
</template>
<script>
import axios from 'axios'

export default {
  asyncData(context){
    return axios.get('https://szfm-beadando-db-default-rtdb.europe-west1.firebasedatabase.app/posts/'+ context.params.id + '.json')
    .then(res => {
      return {
        loadedPost: res.data
      }
    })
    .catch(e => context.error(e))

  },
  
}
</script>

<style scoped>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}

.post {
  width: 100%;
}

@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}

.post-title {
  margin: 0;
}

.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  
}

@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}

.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}

.post-feedback a {
  color:salmon;
  text-decoration: none;
}

.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}
.post-thumbnail {
  margin: 15px;
  width: 100%;
  height: 700px;
  background-position: center;
  background-size: cover;
}
.post-previewText {
  font-size: 3em;
  color:lawngreen;
  margin: 0 10px;
}
</style>
