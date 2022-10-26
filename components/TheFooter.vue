<template lang="">
    <v-footer color="transparent" elevation="0">
    <p class="name">find me in:</p>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/" class="text-decoration-none"><p class="ri-twitter-fill"></p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/about" class="text-decoration-none"><p class="ri-facebook-fill"></p></nuxt-link>
    <v-divider class="mx-4" vertical></v-divider>
    
    <v-spacer></v-spacer>
    <v-divider class="mx-4" vertical></v-divider>
    <nuxt-link to="/contact" class="text-decoration-none"><p>@becardine <i class="ri-github-fill"></i> </p></nuxt-link>
    </v-footer>
</template>
<script>
export default {
    
}
</script>
<style lang="sass" scoped>
p
  margin: 0 
</style>