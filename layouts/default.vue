<template>
  <v-app>
    <!-- navigation bar -->
    <v-navigation-drawer permanent app>
      <v-list> Logo </v-list>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!--  -->
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',

  data() {
    return {
      items: [
        { title: 'Home', icon: 'mdi-home-variant-outline' },
        { title: 'Inbox', icon: 'mdi-inbox' },
        { title: 'Class', icon: 'mdi-video-box' },
        { title: 'Students', icon: 'mdi-account-school' },
        { title: 'Tests', icon: 'mdi-book-open-page-variant' },
        { title: 'Files', icon: 'mdi-file-settings' },
        { title: 'Settings', icon: 'mdi-cog' },
      ],
    }
  },
}
</script>
