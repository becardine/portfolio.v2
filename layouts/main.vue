<template>
  <v-app dark>
    <TheHeader v-if="$vuetify.breakpoint.mdAndUp" />
    <TheHeaderMobile v-else />
    <v-main class="overflow-hidden">
      <div class="cursor"></div>
      <router-view></router-view>
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
  mounted() {
    let mouseCursor = document.querySelector(".cursor");
    window.addEventListener("mousemove", cursor);

    function cursor(e) {
      mouseCursor.style.top = e.pageY + "px";
      mouseCursor.style.left = e.pageX + "px";
    }
  },
};
</script>
<style lang="sass">
.cursor
  width: 16rem,
  height: 16rem,
  border-radius: 50%,
  background: $gradient-2,
  opacity: 0.4,
  filter: blur(50px),
  position: absolute,
  transform: translate(-50%, -50%),
  pointer-events: none

</style>
