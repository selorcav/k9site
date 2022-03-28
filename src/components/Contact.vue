<template>
  <div class="pa-0">
    <v-row class="pa-0 ma-0 orange darken-4 contact">
      <v-col cols="12" md="5">
        <v-container class="mt-8 pa-10 pb-0">
          <div>
            <h4 class="white--text text-h4">Contacto</h4>
            <hr class=" mt-2 mb-8" style="width: 3em">
            <div class="d-flex align-center my-4">
              <v-icon class="white--text">mdi-map-marker</v-icon> 
              <p class="my-0 mx-4 ubuntu white--text text-body-1">742 Evergreen Terrace</p>
            </div>
            <div class="d-flex align-center my-4">
              <v-icon class="white--text">mdi-phone</v-icon> 
              <a href="tel:+5691234567"><p class="my-0 mx-4 ubuntu white--text text-body-1">+569 123 4567</p></a>
            </div>
            <div class="d-flex align-center my-4">
              <v-icon class="white--text">mdi-email</v-icon> 
              <a href="mailto:K9@gmail.com"><p class="my-0 mx-4 ubuntu white--text text-body-1">K9@gmail.com</p></a>
            </div>
          </div>
          <div>
            <v-img class="mb-4 mt-16" width="60%" src="../assets/logos-04.png" />
            <p class="caption white--text">Todos los derechos reservados @2022 </p>
          </div>
        </v-container>
      </v-col>
      <v-col cols="12" md="7">
        <v-container class="pa-2 pa-md-12" >
          <v-card class="pa-4">
            <h3 class="text-h3 ubuntu text-center mt-8">¡Hablemos!</h3>
            <p class="text-body-1 text-center ubuntu mt-6">¿Tienes alguna idea y quieres comenzar un proyecto? ¡Contáctanos! </p>
            <v-form
              ref="form"
              v-model="valid"
              lazy-validation
            >
              <v-row>
                <v-col class="px-8" cols="12" sm="6">
                  <v-text-field
                    v-model="name"
                    :counter="10"
                    :rules="nameRules"
                    label="Name"
                    required
                    prepend-icon="mdi-account"
                  ></v-text-field>
                </v-col>
                <v-col class="px-8" cols="12" sm="6">
                  <v-text-field
                    v-model="email"
                    :rules="emailRules"
                    label="E-mail"
                    required
                    prepend-icon="mdi-email"
                  ></v-text-field>
                </v-col>
                <v-col class="px-8" cols="12">
                  <v-text-field
                    :counter="10"
                    label="Asunto"
                    required
                    prepend-icon="mdi-book-open-blank-variant"
                  ></v-text-field>
                </v-col>
                <v-col class="px-10" cols="12">
                  <v-textarea
                    name="input-7-1"
                    label="Tu Mensaje"
                    value=""
                    hint="Hint text"
                  ></v-textarea>
                </v-col>
              </v-row>
              <div class="d-flex justify-end px-8">
                <v-btn
                  elevation="2"
                  class="orange darken-4 white--text rounded-pill"
                >
                Enviar
                </v-btn>
              </div>
            </v-form>
          </v-card>
        </v-container>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
    },

}
</script>

<style lang="sass" scoped>
@import "../assets/css/main"
.contact
  height: 100%
  background-image: url('../assets/img/bg-14.svg')
  background-size: cover

</style>