<template>
  <div>
    <ion-card v-for="post in posts" :key="post.data.id" style="border: 1px solid blue;">
      <ion-card-content>
        <template v-if="post.data.thumbnail.startsWith('https')">
          <img :src="post.data.thumbnail">
        </template>
        <ion-label color="light">{{ post.data.title }}</ion-label>
      </ion-card-content>
      <ion-button color="tertiary" expand="full" @click="viewMore">View More</ion-button>
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
  async mounted() {
    const response = await axios.get("https://www.reddit.com/r/halo.json");
    this.posts = response.data.data.children;
    console.log(this.posts);
  },
  methods: {
    viewMore() {}
  }
};
</script>
