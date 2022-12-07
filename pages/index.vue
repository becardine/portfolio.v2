<template>
    <v-container class="fill-height" justify="center">
      <v-row justify="center" align="center">
        <v-col :cols="$vuetify.breakpoint.mdAndUp ? 6 : 10">
          <h3 class="font-weight-light">Hi. I am</h3>
          <h2 class="font-weight-light my-n4 ml-n1">becardine</h2>
          <h1 class="font-weight-medium mb-16">> Front-end developer</h1>
          <p v-if="$vuetify.breakpoint.mdAndUp">
            // complete the game
          </p>
          <p class="my-2">
            //
            {{
              $vuetify.breakpoint.mdAndUp
                ? "you can also see it on my Github page"
                : "find my profile on Github:"
            }}
          </p>
          <p>
            <span class="const">const</span>
            <span class="git">githubLink</span> =
            <a v-if="$vuetify.breakpoint.mdAndUp" href="https://github.com/becardine/portfolio.v2/blob/main/components/Gamer.vue" target="_blank" class="link"
              >“https://github.com/becardine/gamer”</a
            >
            <a v-else href="https://github.com/becardine/" target="_blank" class="link"
              >“https://github.com/becardine/”</a
            >
          </p>
        </v-col>
        <v-col cols="6" v-if="$vuetify.breakpoint.mdAndUp">
          <Gamer />
        </v-col>
      </v-row>
    </v-container>
</template>

<script>
export default {
  name: "IndexPage",
  layout: 'main',
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

.row
  max-width: 1240px !important

.container
  justify-content: center
</style>
