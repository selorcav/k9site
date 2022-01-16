<template>
  <v-container class="about-us d-flex justify-center align-center py-12">
    <v-row class="flex-column flex-md-row">
      <v-col cols="12" md="6">
        <div class="px-16 px-md-4">
          <v-img src="../assets/img/pj.svg" />
        </div>
      </v-col>
      <v-col cols="12" class="d-flex flex-column justify-center px-10" md="6">
        <h1 class="main-title font-weight-bold primary-text ubuntu text-center text-md-start">NUESTRA MISIÓN</h1>
        <h2 class="main-subtitle mt-2 font-weight-regular text-center text-md-start mt-5">Ayudar a cerrar la brecha entre el negocio y los datos aprovechando el uso de la inteligencia artificial.</h2>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style lang="sass">
.about-us
  min-height: 100vh
  background-image: url('../assets/img/bg-14.jpg')
  background-size: cover
</style>