<template>
  <v-container align-center justify-center row fill-height fluid class="pa-0 ma-0">
    <side-menu />
    <main-container />
  </v-container>
</template>

<script>
import SideMenu from "../components/SideMenu/SideMenu";
import MainContainer from "../components/MainContainer";

export default {
  name: "home",
  components: {
    SideMenu,
    MainContainer
  }
};
</script>
