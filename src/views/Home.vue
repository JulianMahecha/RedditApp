<template>
  <ion-card>
    <ion-item>
      <ion-label position="floating">Nombre</ion-label>
      <ion-input @input="greeting = $event.target.value"></ion-input>
    </ion-item>
    <ion-button color="tertiary" expand="full" @click="handleClick">Hello</ion-button>
  </ion-card>
</template>

<script>
export default {
  data() {
    return {
      greeting: ""
    };
  },
  methods: {
    handleClick() {
      this.$ionic.alertController
        .create({
          header: "alert",
          subHeader: "subtitle",
          message: this.greeting,
          buttons: ["Ok"]
        })
        .then(a => a.present());
    }
  }
};
</script>
