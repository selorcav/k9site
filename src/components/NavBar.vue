<template>
  <div>
    <v-app-bar fixed class="primary-bg d-flex flex-column justify-center px-2 px-md-0" dark min-height="50px">
      <div>
        <v-img width="181" src="../assets/logos-04.png" />
      </div>
      <v-spacer />
      <v-app-bar-nav-icon class="d-block d-md-none" @click="drawer = true"></v-app-bar-nav-icon>
      <div class="d-none d-md-block">
        <a href="#home"><v-btn class="primary-bg open-sans" elevation="0">Inicio</v-btn></a>
        <a href="#services"><v-btn class="primary-bg open-sans" elevation="0">Servicios</v-btn></a>
        <a href="#aboutus"><v-btn class="primary-bg open-sans" elevation="0">Nosotros</v-btn></a>
        <a href="#contact"><v-btn class="primary-bg open-sans" elevation="0">Contacto</v-btn></a>
      </div>
    </v-app-bar>

    <v-navigation-drawer class="primary-bg" dark v-model="drawer" fixed temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
        >
          <div class="mb-5 px-5">
            <v-img width="181" src="../assets/logos-04.png" />
          </div>
          <v-list-item>
            <v-list-item-title class="body-1 px-5 open-sans" @click="drawer = !drawer"><a class="white--text" href="#home">Inicio</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="body-1 px-5 open-sans" @click="drawer = !drawer"><a class="white--text" href="#services">Servicios</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="body-1 px-5 open-sans" @click="drawer = !drawer"><a class="white--text" href="#aboutus">Nosotros</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="body-1 px-5 open-sans" @click="drawer = !drawer"><a class="white--text" href="#contact">Contacto</a></v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>

<style lang="scss">
@import "../assets/css/main";
.v-application .open-sans{
  font-family: 'Open Sans', sans-serif !important

}


</style>
