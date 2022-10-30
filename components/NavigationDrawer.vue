<template>
    <v-row class="fill-height" no-gutters>
      <v-navigation-drawer
        dark
        mini-variant
        mini-variant-width="56"
        permanent
        color="transparent"
      >
        <v-list dense flat>
          <v-list-item-group v-model="selectedItem" color="secondary">
            <v-list-item v-for="(item, i) in items" :key="i">
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

      <v-list class="grow">
        <v-list-item v-for="(text, i) in items" :key="i" link>
          <v-list-item-title v-text="text.text"></v-list-item-title>
        </v-list-item>
      </v-list>
    </v-row>
</template>
<script>
export default {
  data() {
    return {
      selectedItem: 1,
      items: [
        { text: 'Real-Time', icon: 'ri-terminal-box-fill' },
        { text: 'Audience', icon: 'ri-user-4-fill' },
        { text: 'Conversions', icon: 'ri-gamepad-fill' },
      ],
    };
  },
};
</script>
