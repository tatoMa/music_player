<template>
  <v-layout column>
    <v-layout row>
      <v-flex xs4>
        <div class="display-1 font-weight-bold">What's hot this weekend?</div>
        <div
          class="caption font-weight-light mt-2"
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus eius quidem doloremque qui voluptatum</div>
      </v-flex>
    </v-layout>
    <v-layout row align-center>
      <v-btn
        round
        color="light-blue darken-1"
        dark
      >&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbspListen&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp</v-btn>
      <v-btn color="white" fab dark small class="listen-button">
        <v-icon color="light-blue darken-1">mdi-play</v-icon>
      </v-btn>

      <v-btn color="light-blue darken-1" fab small dark>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
    </v-layout>
  </v-layout>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.listen-button {
  position: relative;
  right: 40px;
}
</style>