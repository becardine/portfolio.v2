<template lang="">
  <v-footer app color="background" elevation="0" class="p-0">
    <p class="name ml-2">find me in:</p>
    <v-divider class="mx-4" vertical></v-divider>
    <a
      href="https://linkedin.com/in/becardine/"
      target="_blank"
      class="text-decoration-none d-flex align-center"
      ><p class="ri-linkedin-fill"></p
    ></a>
    <v-divider class="mx-4" vertical></v-divider>
    <a
      href="https://instagram.com/becardine/"
      target="_blank"
      class="text-decoration-none d-flex align-center"
      ><p class="ri-instagram-fill"></p
    ></a>
    <v-divider class="mx-4" vertical></v-divider>

    <v-spacer></v-spacer>
    <v-divider class="mx-4" vertical></v-divider>
    <a
      href="https://github.com/becardine/"
      target="_blank"
      class="text-decoration-none d-flex align-center mr-2"
    >
      <p class="mr-2" v-if="$vuetify.breakpoint.mdAndUp">@becardine</p>
      <p><i class="ri-github-fill"></i></p>
    </a>
  </v-footer>
</template>
<script>
export default {};
</script>
<style lang="sass" scoped>
p
  margin: 0

.v-footer
    border-top: 1px solid $lines !important,
    padding: 0,

.v-application .background
    border: none
</style>
