<template>
  <div class="orange darken-4">
    <v-container >
      <h3 class="text-h4 text-md-h3 text-center mt-8 white--text ubuntu font-weight-medium team-title position-relative">Nuestros Clientes</h3>
      <p class="white--text"></p>
      <v-row class="mt-16 justify-center">
        <v-col v-for="client in clients" :key="client.id" cols="12" class="pa-8 pa-md-16" sm="4">
          <v-img :src="client.foto"></v-img>
          <p class="my-4 white--text font-italic text-center">"{{client.mensaje}}"</p>
          <p class="my-4 text-center white--text font-weight-bold">{{client.nombre}}</p>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clients: [
        {foto: require("../assets/img/riverine.png") ,nombre: "Riverine", mensaje:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad, odio?"},
        {foto: require("../assets/img/riverine.png") ,nombre: "Riverine", mensaje:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad, odio?"},
        {foto: require("../assets/img/riverine.png") ,nombre: "Riverine", mensaje:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad, odio?"},
      ]
    }
  },
}
</script>

<style lang="sass" scoped>
.team-title:before
  position: absolute
  content: ''
  height: 6px
  width: 80px
  background: #FFF
  bottom: -.8em
  left: calc(50% - 40px)
.position-relative
  position: relative

</style>