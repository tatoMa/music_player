<template>
  <v-flex class="player-section">
    <v-layout row align-center>
      <v-layout row>
        <v-flex xs2>
          <v-img
            :src="require('../../assets/covers/cover1.jpg')"
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
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>