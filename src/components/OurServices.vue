<template>
  <div class="our-services pa-4 pa-sm-6 pa-md-10 pa-lg-16">
    <v-card elevation="0" class="pa-2 pa-sm-4 pa-md-8">
      <div class="position-relative">
        <h2
        class="text-center text-md-h4 font-weight-bold pa-4 service-title bg-primary ubuntu blue-grey--text text--darken-3"
        >
        Nuestros servicios
        </h2>
      </div>
      <v-row class="mt-8 pa-2 pa-sm-4 pa-md-12 justify-center">
        <v-col cols="6" sm="6" md="4" lg="3">
          <v-col v-for="service in services1" :key="service.id"  cols="12" sm="12">
            <v-hover v-slot="{ hover }">
              <v-card class="card-service overflow-hidden">
                <div class="pa-2 pa-sm-4 pa-md-8">
                  <v-img class="mx-auto mt-8" width="50%" :src="service.src" />
                  <v-card-title class="position-relative mx-auto d-block ubuntu font-weight-bold text-center service-title text-subtitle-1 text-md-h6"> {{service.nombre}} </v-card-title>
                  <v-chip-group class="mt-4 text-center " column>
                    <v-chip class="text-caption mx-auto orange darken-1 white--text" v-for="ficha in service.fichas" :key="ficha.id">{{ficha}}</v-chip>
                  </v-chip-group>
                </div>
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out orange darken-4 bg-card-white v-card--reveal white--text pa-4 text-center ubuntu text-caption text-sm-body-1 "
                    style="height: 100%;"
                  >
                    {{service.texto}}
                  </div>
                </v-expand-transition>
              </v-card>
            </v-hover>
          </v-col>                  
        </v-col>
        <v-col cols="6" sm="6" md="4" lg="3">
          <v-col v-for="service in services2" :key="service.id"  cols="12" sm="12">
            <v-hover v-slot="{ hover }">
              <v-card class="card-service overflow-hidden">
                <div class="pa-2 pa-sm-4 pa-md-8">
                  <v-img class="mx-auto mt-8" width="50%" :src="service.src" />
                  <v-card-title class="position-relative mx-auto d-block ubuntu font-weight-bold text-center service-title text-subtitle-1 text-md-h6"> {{service.nombre}} </v-card-title>
                  <v-chip-group class="mt-4 text-center " column>
                    <v-chip class="text-caption mx-auto orange darken-1 white--text" v-for="ficha in service.fichas" :key="ficha.id">{{ficha}}</v-chip>
                  </v-chip-group>
                </div>
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out orange darken-4 bg-card-white v-card--reveal white--text pa-4 text-center ubuntu text-caption text-sm-body-1 "
                    style="height: 100%;"
                  >
                    {{service.texto}}
                  </div>
                </v-expand-transition>
              </v-card>
            </v-hover>
          </v-col>                  
        </v-col>
        <v-col cols="6" sm="6" md="4" lg="3">
          <v-col v-for="service in services3" :key="service.id"  cols="12" sm="12">
            <v-hover v-slot="{ hover }">
              <v-card class="card-service overflow-hidden">
                <div class="pa-2 pa-sm-4 pa-md-8">
                  <v-img class="mx-auto mt-8" width="50%" :src="service.src" />
                  <v-card-title class="position-relative mx-auto d-block ubuntu font-weight-bold text-center service-title text-subtitle-1 text-md-h6"> {{service.nombre}} </v-card-title>
                  <v-chip-group class="mt-4 text-center " column>
                    <v-chip class="text-caption mx-auto orange darken-1 white--text" v-for="ficha in service.fichas" :key="ficha.id">{{ficha}}</v-chip>
                  </v-chip-group>
                </div>
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out orange darken-4 bg-card-white v-card--reveal white--text pa-4 text-center ubuntu text-caption text-sm-body-1 "
                    style="height: 100%;"
                  >
                    {{service.texto}}
                  </div>
                </v-expand-transition>
              </v-card>
            </v-hover>
          </v-col>                  
        </v-col>
        <v-col cols="6" sm="6" md="4" lg="3">
          <v-col v-for="service in services4" :key="service.id"  cols="12" sm="12">
            <v-hover v-slot="{ hover }">
              <v-card class="card-service overflow-hidden">
                <div class="pa-2 pa-sm-4 pa-md-8">
                  <v-img class="mx-auto mt-8" width="50%" :src="service.src" />
                  <v-card-title class="position-relative mx-auto d-block ubuntu font-weight-bold text-center service-title text-subtitle-1 text-md-h6"> {{service.nombre}} </v-card-title>
                  <v-chip-group class="mt-4 text-center " column>
                    <v-chip class="text-caption mx-auto orange darken-1 white--text" v-for="ficha in service.fichas" :key="ficha.id">{{ficha}}</v-chip>
                  </v-chip-group>
                </div>
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out orange darken-4 bg-card-white v-card--reveal white--text pa-4 text-center ubuntu text-caption text-sm-body-1 "
                    style="height: 100%;"
                  >
                    {{service.texto}}
                  </div>
                </v-expand-transition>
              </v-card>
            </v-hover>
          </v-col>                  
        </v-col>

      </v-row>
    </v-card>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: Boolean,
      services1: [
        {nombre: "Producto", texto: "Analizamos tus objetivos de negocio y te proponemos soluciones de IA para alcanzarlos.", src: require("../assets/img/icon-1.svg"), fichas: ["Objetivo", "Solución", "Iteración"]},
        {nombre: "Data", texto: "Exploramos y procesamos tu datos para darte conocimiento de tu negocio.", src: require("../assets/img/icon-4.svg"),fichas: ["Organización", "Empaquetamiento", "Documentación","Logging","Styling"]},
        ],
      services2: [
        {nombre: "Modeling", texto: "Entrenamos modelos de aprendizaje automático y los optimizamos en función de tu métrica de negocio.", src: require("../assets/img/icon-7.svg"),fichas: ["Git", "Pre-Commit", "Versionamiento", "Docker"]},
        {nombre: "Scripting", texto: "Te aseguramos las mejores prácticas de programación.", src: require("../assets/img/icon-2.svg"), fichas: ["Etiquetado","Preprocesamiento","Exploración","Aumento de datos"]},
      ],
      services3: [
        {nombre: "Interfaces", texto: "Construimos interfaces que permitan conectar las soluciones de IA con tus productos.", src: require("../assets/img/icon-5.svg"),fichas: ["CLI", "API"]},
        {nombre: "Testing", texto: "Ponemos a prueba todos los componentes de los sistemas de IA para asegurar de que perduren en el tiempo.", src: require("../assets/img/icon-8.svg"), fichas: ["Dashboard", "CI/CD Workflows", "Feature Stores", "Despliegue", "Monitoreo"]},
      ],
      services4:[
        {nombre: "Producción", texto: "Contamos con un stack completo para asegurar que las soluciones de IA en producción sean integrales.", src: require("../assets/img/icon-6.svg"),fichas: ["Código","Datos","Modelos"]},
        {nombre: "Reproductibilidad", texto: "Nos aseguramos que todas nuestras soluciones de IA se puedan replicar de manera sencilla.", src: require("../assets/img/icon-3.svg"),fichas: ["Base de negocio","Seguimiento","Optimización"] },
      ]
    }
  },
};
</script>

<style lang="sass">
@import "../assets/css/main"
.our-services
  background-image: url('../assets/img/bg-3-1.svg')
  min-height: 100vh
  width: 100%
  background-size: cover
  background-position: center

.card-service
  background-image: url('../assets/img/bg-card-02.svg')
  background-size: cover
  background-position: center
  height: 100%

.bg-card-white
  background-image: url('../assets/img/bg-card-02-white.svg')
  background-size: cover
  background-position: center

.service-title:before
  position: absolute
  content: ''
  height: 6px
  width: 80px
  background: $primary
  bottom: 0
  left: calc(50% - 40px)

.v-application .ubuntu
  font-family: 'Ubuntu', sans-serif !important
.position-relative
  position: relative


.v-card--reveal 
  align-items: center
  top: 0
  justify-content: center
  opacity: 1
  position: absolute
  width: 100%

</style>
