<template>
  <div class="my-2">
    <div class="font-weight-black ml-4">{{title}}</div>
    <v-list dense class="side-menu-groups">
      <v-list-tile v-for="(item,index) in listData" :key="index" @click class="side-menu-item">
        <v-list-tile-content>
          <v-layout row align-center justify-center>
            <v-icon color="grey darken-1" class="mr-3 ml-1">{{item.icon}}</v-icon>

            <v-list-tile-title class="font-weight-medium caption">{{item.name}}</v-list-tile-title>
          </v-layout>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </div>
</template>

<script>
export default {
  name: "MenuGroupList",
  props: ["listData", "title"]
};
</script>

<style lang="scss" scoped>
.side-menu-groups {
  background-color: rgba(0, 0, 0, 0);
}
.side-menu-item {
  transition: 0.03s;

  &:hover {
    color: rgb(117, 172, 255);
    text-shadow: 0 0 10px rgba(245, 247, 228, 0.843);
    transition-delay: 0s;
    transition: 0.01s;
  }
}
</style>