<template>
  <v-row dense class="fill-height">
    <v-col sm="12" md="2" v-if="$vuetify.breakpoint.mdAndUp">
      <v-navigation-drawer
        dark
        mini-variant
        mini-variant-width="370"
        permanent
        color="transparent"
      >
        <div
          class="titleContact d-flex align-center"
          @click="isShowing = !isShowing"
          role="button"
        >
          <v-icon class="mx-3">{{
            isShowing ? "ri-arrow-down-s-fill" : "ri-arrow-up-s-fill"
          }}</v-icon>
          <p class="mb-0 projects">projects</p>
        </div>
        <div v-if="isShowing" class="pa-3 pl-8">
          <v-card width="100%" color="transparent" elevation="0">
            <v-checkbox
              v-for="(tech, idx) in technologies"
              :key="idx"
              color="secondary"
              v-model="selected"
              :label="tech.name"
              :value="tech.value"
              class="mb-n2"
            ></v-checkbox>
          </v-card>
        </div>
      </v-navigation-drawer>
    </v-col>
    <v-col sm="12" md="10">
      <div
        class="titleContact d-flex align-center px-3"
        v-if="$vuetify.breakpoint.mdAndUp"
      >
        <p v-for="(select, idx) in selected" :key="idx" class="mb-0 mx-2">
          {{ select }};
        </p>
        <v-icon
          dark
          left
          color="secondary"
          v-show="selected.length > 0"
          role="button"
          class="mx-2"
          @click="clearSelected"
        >
          ri-close-line
        </v-icon>
        <v-divider
          vertical
          class="ml-2"
          v-show="selected.length > 0"
        ></v-divider>
      </div>
      <div
        class="d-flex flex-wrap"
        :class="$vuetify.breakpoint.mdAndUp ? 'mt-10 ml-10' : 'pa-3'"
      >
        <span
          v-for="(project, idx) in filteredList"
          :key="idx"
          class="mt-5"
          :class="$vuetify.breakpoint.mdAndUp ? 'mx-2' : 'mx-auto my-5'"
        >
          <p>
            <span class="font-weight-medium">Project {{ idx + 1 }}</span> // _{{
              project.title
            }}
          </p>
          <v-card
            class="rounded card"
            color="background"
            max-width="300"
            height="325"
          >
            <v-img :src="project.image" height="150px"></v-img>

            <!-- <v-icon class="tech pa-2 rounded" color="black"
              >ri-vuejs-fill</v-icon
            > -->

            <v-card-subtitle class="description pt-5 px-5">
              {{ project.description }}
            </v-card-subtitle>

            <v-card-actions class="px-4">
              <a :href="project.link" target="_blank" rel="noopener noreferrer">
                <p
                  role="button"
                  class="ml-2 pa-2 px-3 secondaryLight white--text rounded btn"
                >
                  view-project
                </p>
              </a>

              <!-- <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? "mdi-chevron-up" : "mdi-chevron-down"
                }}</v-icon>
              </v-btn> -->
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  {{ project.readMore }}
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </span>
      </div>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: "About",
  layout: "main",
  data() {
    return {
      isShowing: false,
      show: false,
      selected: [],
      technologies: [
        { name: "HTML", value: "html" },
        { name: "CSS", value: "css" },
        { name: "Vue.js", value: "vue" },
        { name: "Nuxt.js", value: "nuxt" },
        { name: "PHP", value: "php" },
        { name: "Laravel", value: "laravel" },
        { name: "Wordpress", value: "wordpress" },
      ],
      projects: [
        {
          title: "nakamura",
          image: "/screenshots/nakamura.jpg",
          link: "https://github.com/becardine/food-api",
          stack: "laravel",
          description:
            "institutional website with table reservations and administrative dashboard.",
          readMore:
            "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! escape.",
        },
        {
          title: "appnews",
          image: "/screenshots/app-news.png",
          stack: "wordpress",
          description:
            "landing page created in order to demonstrate a news application.",
          readMore:
            "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! escape.",
        },
        {
          title: "cardi & alves",
          image: "/screenshots/cardi-alves.png",
          stack: "wordpress",
          description: "institutional website creation for lawyers.",
          readMore:
            "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! escape.",
        },
      ],
    };
  },
  computed: {
    filteredList() {
      let stacks = this.projects.filter((t) => {
        if (this.selected.length < 1) {
          return t;
        } /* else {
          for (const e of this.selected) {
            const s = e.value;
            stacks.push(s);
          }
          stacks.push(this.selected);
        } */
      });
      return stacks;
    },
  },

  methods: {
    clearSelected() {
      this.selected = [];
    },
  },
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

p.projects
  color: white,
  font-size: 1rem

.tech
  background-color: $secondary-2
  font-size: 20px
  position: absolute
  top: 10px
  right: 10px

p > span
  color: $secondary-3

.v-application .background
  border: 1.5px solid #1C2B3A !important

.description
  border-top: 1.5px solid #1C2B3A !important

p.btn
  font-size: 14px
</style>
