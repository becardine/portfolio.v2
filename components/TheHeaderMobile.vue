<template>
  <v-container>
    <v-row align="center">
        <p class="name ml-2">becardine</p>
        <v-spacer></v-spacer>
          <p class="mr-2" role="button">
            <i class="ri-menu-line"></i>
          </p>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data: () => ({ value: 1 }),
};
</script>
<style lang="sass" scoped>
p
  margin: 0

.isActive
  color: $accent-3
</style>
