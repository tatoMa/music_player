<template>
  <v-layout class="cover-top-menu mt-4" row>
    <v-flex xs5>
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
    </v-flex>
    <v-flex xs5></v-flex>
    <v-flex xs2>
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
    </v-flex>
  </v-layout>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>