<template>
  <v-layout column class="cover-section">
    <!-- custom toolbar -->
    <main-toolbar />
    <main-info />
    <new-albums />
  </v-layout>
</template>

<script>
import NewAlbums from "./NewAlbums";
import MainToolbar from "./MainToolbar";
import MainInfo from "./MainInfo";
export default {
  components: {
    NewAlbums,
    MainToolbar,
    MainInfo
  }
};
</script>

<style lang="scss" scoped>
.cover-section {
  // height: 380px;
  background-color: red;
  // background-image: url("../assets/bg-2.jpg");
  background-image: radial-gradient(rgba(255, 255, 255, 0), #000000fc),
    url("../../assets/cover.jpg");
  background-position: top; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
}
</style>