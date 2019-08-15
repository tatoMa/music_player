<template>
  <v-layout align-center class="main-container">
    <v-layout align-center fill-height>
      <v-layout column class="main-menu white--text">
        <!-- Top Section of main menu -->
        <top-section />
        <!-- Playlists section of main menu -->
        <playlists />
        <!-- Player section -->
        <player />
      </v-layout>
      <div class="outer-space"></div>
    </v-layout>
  </v-layout>
</template>

<script>
import TopSection from "./TopSection";
import Player from "./Player";
import Playlists from "./Playlists";
export default {
  components: {
    TopSection,
    Player,
    Playlists
  },
  data: () => ({})
};
</script>
<style lang="scss" scoped>
.main-container {
  background-color: aqua;
  background-image: url("../../assets/bg-2.jpg");
  background-size: cover;
  width: 80%;
  min-width: 1000px;

  .main-menu {
    background-color: rgb(0, 0, 0);
    min-height: 80%;
  }
}
// .listen-button {
//   left: -10px;
// }
.outer-space {
  width: 40px;
}
</style>
