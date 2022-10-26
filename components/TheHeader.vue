<template>
  <v-app-bar app color="transparent" elevation="0">
    <nuxt-link to="/" class="text-decoration-none"><p class="name">becardine</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/" class="text-decoration-none"><p>_hello</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/about" class="text-decoration-none"><p>_about</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/projects" class="text-decoration-none"><p>_projects</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>

    <v-spacer></v-spacer>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/contact" class="text-decoration-none"><p>_contact-me</p></nuxt-link>
  </v-app-bar>
</template>
<script>
export default {
  data: () => ({ value: 1 }),
};
</script>
<style lang="sass" scoped>
v-app-bar
    border-bottom: 1px solid
p
  margin: 0

p.name 
    width: 180px
</style>
