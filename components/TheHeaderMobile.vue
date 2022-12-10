<template>
  <v-app-bar app flat color="background" elevation="0">
    <nuxt-link to="/" class="name ml-2"><p>becardine</p></nuxt-link>
    <v-spacer></v-spacer>
    <v-menu
      offset-y
      bottom
      origin="center center"
      transition="scale-transition"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn elevation="0" color="transparent" v-bind="attrs" v-on="on">
          <i class="ri-menu-line"></i>
        </v-btn>
      </template>
      <v-list dark>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          link
          color="background"
        >
          <nuxt-link :to="{ name: item.link }" class="text-decoration-none"
            ><p>{{ item.title }}</p></nuxt-link
          >
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>
<script>
export default {
  data: () => ({
    value: 1,
    selectedItem: 1,
    items: [
      { title: "home", link: "index" },
      { title: "projects", link: "projects" },
      // { title: "about", link: 'about' },
      { title: "contact", link: "contacte-me" },
    ],
  }),
};
</script>
<style lang="sass" scoped>
p
  margin: 0

.isActive
  color: $accent-3

.theme--dark.v-list
  background-color: $primary-3
</style>
