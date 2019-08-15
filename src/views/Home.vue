<template>
  <v-container align-center justify-center row fill-height fluid class="pa-0 ma-0">
    <v-layout align-center justify-end class="side-container">
      <v-layout align-center fill-height>
        <div class="outer-space"></div>
        <v-layout column align-end class="side-menu">
          <v-flex>Memembership</v-flex>
          <v-flex>Browse Music</v-flex>
          <v-flex>Your Music</v-flex>
          <v-flex>Your Playlists</v-flex>
        </v-layout>
      </v-layout>
    </v-layout>
    <v-layout align-center class="main-container">
      <v-layout align-center fill-height>
        <v-layout column class="main-menu white--text">
          <v-layout column class="cover-section">
            <v-layout class="cover-top-menu mt-4">
              <v-text-field
                dark
                solo
                clearable
                label="Search"
                prepend-inner-icon="mdi-magnify"
                append-icon="mdi-microphone"
                background-color="rgba(255, 255, 255, 0.1)"
                class="ml-5"
              ></v-text-field>
              <v-spacer></v-spacer>

              <v-badge overlap class="mt-3">
                <template v-slot:badge>
                  <span>2</span>
                </template>
                <v-icon dark>mdi-bell</v-icon>
              </v-badge>

              <v-badge overlap class="mx-4">
                <!-- <template v-slot:badge>
                  <span>3</span>
                </template>-->
                <v-avatar>
                  <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
                </v-avatar>
              </v-badge>
            </v-layout>
            <v-flex>
              <div class="display-1">What's hot this weekend?</div>
              <div
                class="caption"
              >Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus eius quidem doloremque qui voluptatum minima impedit tempore explicabo a! Eum non et quo ullam facere in saepe necessitatibus ad repellendus?</div>
              <v-btn round color="primary" dark>Rounded Button</v-btn>
              <v-btn color="warning" fab dark>
                <v-icon>mdi-play</v-icon>
              </v-btn>
              <v-btn color="warning" fab dark>
                <v-icon>mdi-bookmark-outline</v-icon>
              </v-btn>
            </v-flex>
            <v-flex>
              <v-layout>
                <v-flex xs10 class="subheading">Noteworthy Albums</v-flex>
                <v-flex xs2 class="caption">Better recommondation?</v-flex>
              </v-layout>
              <v-layout align-center justify-center row class="mt-1">
                <v-flex xs2 v-for="(i,index) in 6" :key="index" class="mx-2">
                  <v-img
                    :src="require(`../assets/covers/cover${i}.jpg`)"
                    class="image"
                    alt="lorem"
                    width="100%"
                    height="100%"
                  />
                  <v-flex xs2 class="caption font-weight-black">Album{{i}}</v-flex>
                  <v-flex xs2 class="caption font-weight-light">Artist{{i}}</v-flex>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
          <v-layout class="playlist-section mx-2 mt-2" justify-center>
            <v-layout column>
              <v-layout>
                <v-flex xs10 class="font-weight-bold">Latist Songs Releases</v-flex>
                <v-flex xs2>
                  <v-icon dark>mdi-play</v-icon>
                </v-flex>
              </v-layout>

              <v-layout column>
                <v-list dark class="play-list-items">
                  <v-list-tile
                    v-for="(i,index) in 6"
                    :key="index"
                    avatar
                    @click
                    class="play-list-item"
                  >
                    <v-layout row align-center wrap>
                      <v-flex xs1>
                        <span>{{i}}</span>
                        <v-icon dark class="mt-1">mdi-plus</v-icon>
                      </v-flex>
                      <v-flex xs2>
                        <v-img
                          :src="require(`../assets/covers/cover${i}.jpg`)"
                          contain
                          class="image"
                          alt="lorem"
                          width="90%"
                          height="90%"
                          max-height="50px"
                        />
                      </v-flex>
                      <v-flex xs7>
                        <v-flex class="caption font-weight-black">Album{{i}}</v-flex>
                        <v-flex class="caption font-weight-light">Artist{{i}}</v-flex>
                      </v-flex>
                      <v-flex xs1 class="caption font-weight-light">50:34</v-flex>
                      <v-flex xs1>
                        <v-icon dark>mdi-dots-horizontal</v-icon>
                      </v-flex>
                    </v-layout>
                  </v-list-tile>
                </v-list>
              </v-layout>
            </v-layout>

            <v-layout column>
              <v-layout>
                <v-flex xs10 class="font-weight-bold">Latist songle Releases</v-flex>
                <v-flex xs2>
                  <v-icon dark>mdi-play</v-icon>
                </v-flex>
              </v-layout>

              <v-layout column>
                <v-list dark class="play-list-items">
                  <v-list-tile
                    v-for="(i,index) in 6"
                    :key="index"
                    avatar
                    @click
                    class="play-list-item"
                  >
                    <v-layout row align-center wrap>
                      <v-flex xs1>
                        <span>{{i}}</span>
                        <v-icon dark class="mt-1">mdi-plus</v-icon>
                      </v-flex>
                      <v-flex xs2>
                        <v-img
                          :src="require(`../assets/covers/cover${9-i}.jpg`)"
                          contain
                          class="image"
                          alt="lorem"
                          width="90%"
                          height="90%"
                          max-height="50px"
                        />
                      </v-flex>
                      <v-flex xs7>
                        <v-flex class="caption font-weight-black">Album{{i}}</v-flex>
                        <v-flex class="caption font-weight-light">Artist{{i}}</v-flex>
                      </v-flex>
                      <v-flex xs1 class="caption font-weight-light">50:34</v-flex>
                      <v-flex xs1>
                        <v-icon dark>mdi-dots-horizontal</v-icon>
                      </v-flex>
                    </v-layout>
                  </v-list-tile>
                </v-list>
              </v-layout>
            </v-layout>
          </v-layout>
          <v-flex class="player-section">c</v-flex>
        </v-layout>
        <div class="outer-space"></div>
      </v-layout>
    </v-layout>
  </v-container>
</template>

<script>
import HelloWorld from "../components/HelloWorld";

export default {
  components: {
    HelloWorld
  }
};
</script>
<style lang="scss" scoped>
.side-container {
  background-color: burlywood;
  background-image: url("../assets/bg-1.jpg");
  background-size: cover;
  width: 20%;
  min-width: 250px;

  .side-menu {
    background-color: rgba(0, 0, 0, 0.514);
    /* filter: blur(5px); */
    min-height: 80%;
    /* width: 50%; */
  }
}
.main-container {
  background-color: aqua;
  background-image: url("../assets/bg-2.jpg");
  background-size: cover;
  width: 80%;
  min-width: 700px;

  .main-menu {
    background-color: rgb(0, 0, 0);
    min-height: 80%;

    .cover-section {
      // height: 380px;
      background-color: red;
      // background-image: url("../assets/bg-2.jpg");
      background-image: radial-gradient(rgba(255, 255, 255, 0), #000000fc),
        url("../assets/cover.jpg");
      background-position: top; /* Center the image */
      background-repeat: no-repeat; /* Do not repeat the image */
      background-size: cover; /* Resize the background image to cover the entire container */
      .cover-top-menu {
        // height: 20px;
      }
    }
    .playlist-section {
      // height: calc(100% - 420px);
    }
    .player-section {
      // height: 40px;
    }
  }
}
.outer-space {
  width: 40px;
}
.play-list-items {
  background: black;
  height: 200px; /* or any value */
  overflow-y: auto;
}
.play-list-items::-webkit-scrollbar-thumb {
  background-color: #424242;
  border: 2px solid #252525;
}
.play-list-items::-webkit-scrollbar {
  width: 10px;
  background-color: #000000;
}
.play-list-item:hover {
  background: rgb(20, 28, 39);
}
</style>
