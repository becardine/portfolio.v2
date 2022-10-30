<template>
  <v-row dense class="fill-height">
    <v-navigation-drawer
      dark
      mini-variant
      mini-variant-width="56"
      permanent
      color="transparent"
    >
      <v-list dense flat>
        <v-list-item-group v-model="selectedRoute" color="secondary">
          <v-list-item v-for="(item, i) in icons" :key="i">
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-col cols="6">
      <v-navigation-drawer
        dark
        mini-variant
        mini-variant-width="180"
        permanent
        color="transparent"
      >
        <v-list dense flat>
          <v-list-item-group v-model="selectedItem" color="secondary">
            <v-list-item v-for="(title, i) in titles" :key="i">
              <v-list-item-content>
                <v-list-item-title v-text="title.text">
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </v-col>
    <v-col cols="3">jj</v-col>
  </v-row>
</template>
<script>
export default {
  name: "About",
  layout: "main",
  data() {
    return {
      selectedItem: null,
      selectedRoute: 1,
      icons: [
        { icon: "ri-terminal-box-fill" },
        { icon: "ri-user-4-fill" },
        { icon: "ri-gamepad-fill" },
      ],
      titles: [
        { text: "personal-info" },
        { text: "contacts" },
      ],
    };
  },
};
</script>
<style lang="sass" scoped>
.row--dense
    padding: 0px
</style>
