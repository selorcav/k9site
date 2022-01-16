<template>
  <v-app class="overflow-x-hidden">
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
<style lang="sass">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;700&display=swap')
.open-sans
  font-family: 'Open Sans', sans-serif !important
</style>
