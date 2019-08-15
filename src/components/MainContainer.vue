<template>
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
        <v-flex class="player-section">
          <v-layout row align-center>
            <v-layout row>
              <v-flex xs2>
                <v-img
                  :src="require('../assets/covers/cover1.jpg')"
                  contain
                  class="image"
                  alt="lorem"
                  max-height="35px"
                />
              </v-flex>
              <v-flex xs8>
                <v-flex class="caption font-weight-black">AlbumAlbumAlbumAlbum</v-flex>
                <v-flex class="caption font-weight-light">ArtistArtistArtist</v-flex>
              </v-flex>
            </v-layout>
            <v-layout align-center>
              <div class="caption font-weight-light mr-2">1:15</div>
              <v-progress-linear
                color="secondary"
                height="2"
                value="35"
                background-color="blue-grey lighten-5"
              ></v-progress-linear>
              <div class="caption font-weight-light ml-2">-3:20</div>
            </v-layout>
            <v-layout row>
              <v-flex xs6></v-flex>
              <v-flex xs6>
                <v-btn color="blue-grey lighten-1" flat icon dark left>
                  <v-icon>mdi-rewind</v-icon>
                </v-btn>
                <v-btn color="grey lighten-4" fab dark small>
                  <v-icon color="light-blue darken-1">mdi-play</v-icon>
                </v-btn>
                <v-btn color="blue-grey lighten-1" flat icon dark right>
                  <v-icon>mdi-fast-forward</v-icon>
                </v-btn>
              </v-flex>
            </v-layout>
          </v-layout>
        </v-flex>
      </v-layout>
      <div class="outer-space"></div>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  data: () => ({})
};
</script>
<style lang="scss" scoped>
.main-container {
  background-color: aqua;
  background-image: url("../assets/bg-2.jpg");
  background-size: cover;
  width: 80%;
  min-width: 1000px;

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
  &::-webkit-scrollbar-thumb {
    background-color: #424242;
    border: 2px solid #252525;
  }
  &::-webkit-scrollbar {
    width: 10px;
    background-color: #000000;
  }
}
.play-list-item:hover {
  background: rgb(20, 28, 39);
}
</style>
