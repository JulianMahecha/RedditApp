<template>
  <ion-app>
    <ion-toolbar>
      <ion-buttons slot="secondary">
        <ion-button>Ionic</ion-button>
      </ion-buttons>
      <ion-title>IonicVue</ion-title>
    </ion-toolbar>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div> -->
    <ion-content color="dark"><router-view/></ion-content>
  </ion-app>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
