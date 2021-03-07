<template>
  <v-app>
    
    <v-navigation-drawer dark class="deep-purple accent-4" v-model="menu" clipped temporary app bottom>
      <v-btn @click="menu = !menu">
        Close
      </v-btn>
            <v-list>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          class="red"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-btn @click="menu = !menu">
        Drawer
      </v-btn>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    menu: false,
    items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Account', icon: 'mdi-account-box' },
          { title: 'Admin', icon: 'mdi-gavel' },
        ],
  }),
};
</script>
