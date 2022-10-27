<template>
  <v-container class="fill-height">
    <v-row justify="center">
      <v-col cols="8">
        <h3 class="font-weight-light"> Hi. I am</h3>
        <h2 class="font-weight-light my-n4 ml-n1">becardine</h2>
        <h1 class="font-weight-medium mb-16">> Front-end developer</h1>
        <p>// complete the game to continue</p>
        <p class="my-2">// you can also see it on my Github page</p>
        <p>
          <span class="const">const</span> <span class="git">githubLink</span> =
          <a href="https://github.com/becardine/" target="_blank" class="link"
            >“https://github.com/becardine/”</a
          >
        </p>
      </v-col>
      <v-col cols="4"> Game </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "IndexPage",
  layout: "main",
};
</script>
<style lang="sass" scoped>
p
  margin: 0

h2
  font-size: 3.875rem
  color: $text

h3
  color: $text

h1,
.const
  color: $secondary-3

.git
  color: $accent-2

.link
  color: $accent-3
</style>
