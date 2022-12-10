<template>
  <v-row dense class="fill-height">
    <v-navigation-drawer
      dark
      mini-variant
      mini-variant-width="56"
      permanent
      color="transparent"
    >
      <v-list dense flat>
        <v-list-item-group v-model="selectedRoute" color="secondary">
          <v-list-item v-for="(item, i) in icons" :key="i">
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-navigation-drawer
      dark
      mini-variant
      mini-variant-width="370"
      permanent
      color="transparent"
    >
      <div
        class="title d-flex align-center"
        @click="isShowing = !isShowing"
        role="button"
      >
        <i v-if="!isShowing" class="ri-arrow-down-s-fill mx-3"></i>
        <i v-else class="ri-arrow-up-s-fill mx-3"></i>
        <p class="mb-0">personal-info</p>
      </div>
      <div v-if="isShowing" class="pa-3 px-4">
        <v-card
          width="100%"
          color="transparent"
          elevation="0"
          class="d-flex align-center"
        >
          <i class="ri-arrow-right-s-line"></i>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="24"
            height="24"
          >
            <path fill="none" d="M0 0h24v24H0z" />
            <path
              d="M22 8v12a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V7h19a1 1 0 0 1 1 1zm-9.586-3H2V4a1 1 0 0 1 1-1h7.414l2 2z"
              fill="rgba(233,146,135,1)"
            />
          </svg>
          <p class="mb-0 ml-2">bio</p>
        </v-card>
        <v-card
          width="100%"
          color="transparent"
          elevation="0"
          class="d-flex align-center"
        >
          <i class="ri-arrow-right-s-line"></i>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="24"
            height="24"
          >
            <path fill="none" d="M0 0h24v24H0z" />
            <path
              d="M22 8v12a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V7h19a1 1 0 0 1 1 1zm-9.586-3H2V4a1 1 0 0 1 1-1h7.414l2 2z"
              fill="rgba(67,217,173,1)"
            />
          </svg>
          <p class="mb-0 ml-2">interests</p>
        </v-card>
        <v-card
          width="100%"
          color="transparent"
          elevation="0"
          class="d-flex align-center"
        >
          <i class="ri-arrow-right-s-line"></i>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="24"
            height="24"
          >
            <path fill="none" d="M0 0h24v24H0z" />
            <path
              d="M22 8v12a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V7h19a1 1 0 0 1 1 1zm-9.586-3H2V4a1 1 0 0 1 1-1h7.414l2 2z"
              fill="rgba(58,73,164,1)"
            />
          </svg>
          <p class="mb-0 ml-2">education</p>
        </v-card>
      </div>
      <div
        class="titleContact d-flex align-center"
        @click="(isShowing2 = !isShowing2)"
        role="button"
      >
        <i v-if="!isShowing2" class="ri-arrow-down-s-fill mx-3"></i>
        <i v-else class="ri-arrow-up-s-fill mx-3"></i>
        <p class="mb-0">contacts</p>
      </div>
      <div v-if="isShowing2" class="pa-3 px-4">
        <v-card
          width="100%"
          color="transparent"
          elevation="0"
          class="d-flex align-center"
        >
          <i class="ri-arrow-right-s-line"></i>
          <p class="mb-0 ml-2">contato@becardine.dev</p>
        </v-card>
      </div>
    </v-navigation-drawer>
    dd
  </v-row>
</template>
<script>
export default {
  name: "About",
  layout: "main",
  data() {
    return {
      isShowing: false,
      isShowing2: false,
      selectedItem: null,
      selectedRoute: 1,
      icons: [
        { icon: "ri-terminal-box-fill" },
        { icon: "ri-user-4-fill" },
        { icon: "ri-gamepad-fill" },
      ],
      titles: [{ text: "personal-info" }, { text: "contacts" }],
    };
  },
  watch: {
    isShowing() {
      if(this.isShowing) {
        console.log(this.isShowing)
      }
    }
  }
};
</script>
<style lang="sass" scoped>
.row--dense
    padding: 0px
.title
  border-bottom: 1px solid $lines
  height: 60px

.titleContact
  border-block: 1px solid $lines
  height: 60px

p
  color: white,
  font-size: 1rem
</style>
