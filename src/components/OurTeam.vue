<template>
  <div class="our-team primary-bg">
    <v-container >
      <h3 class="text-h4 text-md-h3 text-center mt-8 white--text ubuntu font-weight-medium team-title position-relative">Nuestro Equipo</h3>
      <v-row class="mt-16">
        <v-col v-for="person in team" :key="person.id" cols="12" class="pa-16" md="4">
          <v-avatar
            color="white"
            width="100%"
            height="auto"
          >
            <v-img :src="person.foto"></v-img>
          </v-avatar>
          <h4 class="mt-6 text-h4 ubuntu white--text text-center"> {{person.nombre}} </h4>
          <p class="text-center mt-2 ubuntu white--text text-body-1"> {{person.cargo}} </p>
          <p class="text-center mt-2 ubuntu white--text text-body-2"> {{person.descripcion}} </p>
          <a href="https://www.linkedin.com/"><v-img width="40" class="mx-auto" src="../assets/img/linkedin-logo.svg"/></a>
        </v-col>
        
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {foto: require("../assets/img/profile1.svg") ,nombre: "John Doe", cargo: "Director", descripcion: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum, perspiciatis."},
        {foto: require("../assets/img/profile2.svg") ,nombre: "Jane Doe", cargo: "Dev", descripcion: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum, perspiciatis."},
        {foto: require("../assets/img/profile3.svg") ,nombre: "John Smith", cargo: "Project Manager", descripcion: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum, perspiciatis."}
      ]
    }
  },

}
</script>

<style lang="sass" scoped>
@import "../assets/css/main"
.our-team
  min-height: 100vh
  background-image: url('../assets/img/bg-3.svg')
  background-position: bottom
  background-size: cover

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