<template>
  <v-app dark>
    <TheHeader v-if="$vuetify.breakpoint.mdAndUp" />
    <TheHeaderMobile v-if="$vuetify.breakpoint.smAndDown" />
    <v-main>
      <Nuxt />
    </v-main>
    <TheFooter />
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {};
  },
};
</script>
