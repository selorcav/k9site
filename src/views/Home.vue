<template>
  <v-app>
    <nav-bar />
    <main-banner id="home" />
    <our-services id="services" />
    <our-mission id="aboutus" />
    <our-team id="ourteam" />
    <clients />
    <contact id="contact"/>
  </v-app>
</template>

<script>
import Clients from '../components/Clients.vue';
import Contact from '../components/Contact.vue';
import MainBanner from '../components/MainBanner.vue';
import NavBar from '../components/NavBar.vue';
import OurMission from '../components/OurMission.vue';
import OurServices from '../components/OurServices.vue';
import OurTeam from '../components/OurTeam.vue';
export default {
  components: { MainBanner, NavBar, OurServices, OurMission, OurTeam, Contact, Clients},
  name: "Home",

};
</script>

