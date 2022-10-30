<template>
  <v-app-bar app color="background" elevation="0">
    <p class="name ml-2">becardine</p>
    <v-spacer></v-spacer>
    <div>
    <p class="mr-2" role="button">
    <i class="ri-align-justify"></i>
    </p>
    </div>
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
