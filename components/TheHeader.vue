<template>
  <v-app-bar app color="transparent" elevation="0">
    <p class="name ml-2">becardine</p>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/" class="text-decoration-none"><p :class="{ isActive: $route.name === 'index'}">_hello</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/about" class="text-decoration-none"><p :class="{ isActive: $route.name === 'about'}">_about</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/projects" class="text-decoration-none"><p :class="{ isActive: $route.name === 'projects'}">_projects</p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>

    <v-spacer></v-spacer>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/contact" class="text-decoration-none mr-2"><p :class="{ isActive: $route.name === 'contact'}">_contact-me</p></nuxt-link>
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

.isActive 
  color: $accent-3
</style>
