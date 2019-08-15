<template>
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
          <v-list-tile v-for="(i,index) in 6" :key="index" avatar @click class="play-list-item">
            <v-layout row align-center wrap>
              <v-flex xs1>
                <span>{{i}}</span>
                <v-icon dark class="mt-1">mdi-plus</v-icon>
              </v-flex>
              <v-flex xs2>
                <v-img
                  :src="require(`../../assets/covers/cover${i}.jpg`)"
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
          <v-list-tile v-for="(i,index) in 6" :key="index" avatar @click class="play-list-item">
            <v-layout row align-center wrap>
              <v-flex xs1>
                <span>{{i}}</span>
                <v-icon dark class="mt-1">mdi-plus</v-icon>
              </v-flex>
              <v-flex xs2>
                <v-img
                  :src="require(`../../assets/covers/cover${9-i}.jpg`)"
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
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
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