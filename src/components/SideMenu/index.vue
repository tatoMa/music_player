<template>
  <v-layout align-center justify-end class="side-container">
    <v-layout align-center fill-height>
      <div class="outer-space"></div>

      <!-- side menu -->
      <v-layout column class="side-menu">
        <div class="side-menu-groups">
          <!-- section 1 -->
          <div>
            <v-btn outline>Memembership</v-btn>
          </div>

          <!-- section 2 -->
          <menu-list-group :listData="browseMusic" title="Browse Music" />
          <v-divider></v-divider>

          <!-- section 3 -->
          <menu-list-group :listData="yourMusic" title="Your Music" />
          <v-divider></v-divider>

          <!-- section 4 -->
          <menu-list-group :listData="yourPlaylist" title="Your Playlist" />
        </div>
      </v-layout>
    </v-layout>
  </v-layout>
</template>

<script>
import MenuListGroup from "./MenuListGroup";
export default {
  name: "SideMenu",
  components: { MenuListGroup },
  data: () => ({
    browseMusic: [
      {
        name: "Discover",
        icon: "mdi-animation-play-outline"
      },
      {
        name: "Grooves",
        icon: "mdi-square-inc"
      },
      {
        name: "TopChart",
        icon: "mdi-arrow-up-bold-outline"
      },
      {
        name: "Clubs",
        icon: "mdi-account-multiple-outline"
      },
      {
        name: "Free Music",
        icon: "mdi-headphones"
      },
      {
        name: "Station",
        icon: "mdi-radio-tower"
      }
    ],
    yourMusic: [
      {
        name: "Favoraties",
        icon: "mdi-heart-outline"
      },
      {
        name: "History",
        icon: "mdi-history"
      }
    ],
    yourPlaylist: [
      {
        name: "Public Playlist",
        icon: "mdi-music-circle-outline"
      },
      {
        name: "Purchased",
        icon: "mdi-music"
      },
      {
        name: "My First Playlist",
        icon: "mdi-music-box-outline"
      }
    ]
  })
};
</script>
<style lang="scss" scoped>
.side-container {
  background-image: url("../../assets/bg-1.jpg");
  background-size: cover;
  width: 15%;
  min-width: 200px;

  .side-menu {
    // background-color: rgba(0, 0, 0, 0.7);
    // min-height: 100%;
    position: relative;
    background: inherit;
    border-radius: 2px;
    overflow: hidden;

    &:after {
      content: "";
      background: inherit;
      position: absolute;
      left: -25px;
      right: 0;
      top: -25px;
      bottom: 0;
      box-shadow: inset 0 0 0 200px rgba(0, 30, 36, 0.45);
      filter: blur(5px);
    }
    .side-menu-groups {
      z-index: 5;
    }
  }
}
.outer-space {
  width: 40px;
}
</style>
