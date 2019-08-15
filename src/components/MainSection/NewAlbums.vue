<template>
  <v-flex>
    <v-layout>
      <v-flex xs10 class="subheading">Noteworthy Albums</v-flex>
      <v-flex xs2 class="caption">Better recommondation?</v-flex>
    </v-layout>
    <v-layout align-center justify-center row class="mt-1">
      <v-flex xs2 v-for="(i,index) in 6" :key="index" class="mx-2">
        <v-img
          :src="require(`../../assets/covers/cover${i}.jpg`)"
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
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>