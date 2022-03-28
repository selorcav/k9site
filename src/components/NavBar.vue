<template>
  <div>
    <v-app-bar fixed class="primary-bg d-flex flex-column justify-center px-2 px-md-0" dark min-height="50px">
      <div>
        <v-img width="181" src="../assets/logos-04.png" />
      </div>
      <v-spacer />
      <v-app-bar-nav-icon class="d-block d-md-none" @click="drawer = true"></v-app-bar-nav-icon>
      <div v-for="menu in nav" :key="menu.id" class="d-none d-md-block">
        <a :href="menu.link"><v-btn class="primary-bg open-sans" elevation="0">{{menu.nombre}}</v-btn></a>
      </div>
    </v-app-bar>

    <v-navigation-drawer class="primary-bg" dark v-model="drawer" fixed temporary>
      <v-list nav dense>
        <div class="my-8 px-5">
          <v-img width="181" src="../assets/logos-04.png" />
        </div>
        <v-list-item-group
          v-model="group"
          v-for="menu in nav"
          :key="menu.id"
        >
          <a class="white--text" :href="menu.link">
            <v-btn elevation="0" class="d-block col-12 my-2 primary-bg">
              <v-list-item-title class="body-1 px-5 open-sans" @click="drawer = !drawer">{{menu.nombre}}</v-list-item-title>
            </v-btn>
          </a>
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
    nav: [
      {nombre: "Inicio", link: "#home"},
      {nombre: "Servicios", link: "#services"},
      {nombre: "Nosotros", link: "#aboutus"},
      {nombre: "Nuestro Equipo", link: "#ourteam"},
      {nombre: "Contacto", link: "#contact"},
      ]
  }),
};
</script>

<style lang="scss">
@import "../assets/css/main";
.v-application .open-sans{
  font-family: 'Open Sans', sans-serif !important
}
.v-list-item--link:before{
  background-color: none !important
}

</style>
