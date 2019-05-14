<template>
  <div>
    <ion-card v-for="post in posts" :key="post.data.id">
      <ion-card-content>
        <ion-label >{{ post.data.title }}</ion-label>  
      </ion-card-content>
    </ion-card>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      posts: []
    };
  },
  async mounted(){
    const response = await axios.get('https://www.reddit.com/r/halo.json');
    this.posts = response.data.data.children
  }
};
</script>
