<template>
  <v-main class="mt-16 mt-md-0 main d-flex justify-center align-md-center">
    <v-container >
      <v-row class="flex-column-reverse flex-md-row">
        <v-col cols="12" class="d-flex flex-column justify-center px-10" md="6">
          <h1 class="main-title font-weight-bold primary-text ubuntu text-center text-md-start">Lorem ipsum dolor sit amet consectetur.</h1>
          <h2 class="main-subtitle mt-2 font-weight-regular text-center text-md-start">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laboriosam, cupiditate.</h2>
          <div class="d-flex">
            <a href="#services"><v-btn dark class="primary-bg mx-auto mx-md-0 my-5">Nuestros servicios</v-btn></a>
          </div>
        </v-col>
        <v-col cols="12" md="6">
          <div class="px-16 px-md-4">
            <Illustration />  
          </div>
        </v-col>
      </v-row>
    </v-container>
    <div></div>
  </v-main>
</template>

<script>
import Illustration from '../components/Illustration.vue';
export default {
  name: "Home",

  components: {Illustration},
};
</script>
<style lang="sass" scoped>
.main
  min-height: 100vh
  background-image: url('../assets/img/bg-14.jpg')
  background-size: cover
.ubuntu
  font-family: 'Ubuntu', sans-serif !important

</style>