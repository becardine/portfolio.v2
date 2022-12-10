<template>
  <v-app-bar app flat color="background" elevation="0">
    <nuxt-link :to="{ name: 'index' }" class="text-decoration-none">
      <p class="name ml-2">becardine</p>
    </nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link :to="{ name: 'index' }" class="text-decoration-none"
      ><p :class="{ isActive: $route.name === 'index' }">_hello</p></nuxt-link
    >
    <!-- <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link :to="{ name: 'about' }" class="text-decoration-none"
      ><p :class="{ isActive: $route.name === 'about' }">_about</p></nuxt-link
    > -->
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link :to="{ name: 'projects' }" class="text-decoration-none"
      ><p :class="{ isActive: $route.name === 'projects' }">
        _projects
      </p></nuxt-link
    >
    <v-divider class="mx-4" vertical></v-divider>
    <v-spacer></v-spacer>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link :to="{ name: 'contact-me' }" class="text-decoration-none mr-2"
      ><p :class="{ isActive: $route.name === 'contact-me' }">
        _contact-me
      </p></nuxt-link
    >
  </v-app-bar>
</template>
<script>
export default {
  data: () => ({
    value: 1,
    selectedItem: 1,
    items: [
      { text: "Real-Time", icon: "mdi-clock" },
      { text: "Audience", icon: "mdi-account" },
      { text: "Conversions", icon: "mdi-flag" },
    ],
  }),
};
</script>
<style lang="sass" scoped>
v-app-bar
    border-bottom: 1px solid
p
  margin: 0
  &:hover
    color: $accent-3

p.name
    width: 180px
    &:hover
      color: $secondary

.isActive
  color: $accent-3
</style>
