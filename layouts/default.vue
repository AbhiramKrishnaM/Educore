<template>
  <v-app>
    <!-- navigation bar -->
    <v-navigation-drawer permanent app>
      <v-list flat dense nav class="ml-1 full-height">
        <v-list-item>
          <v-list-item-icon class="mr-4">
            <v-icon>mdi-cog</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Logo</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <div class="spacer-box-1"></div>

        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          :ripple="false"
          :input-value="id === item.id"
          active-class="link-active"
          link
          class="link"
          @click="setCurrentLinkId(item.id)"
        >
          <v-list-item-icon class="mr-4">
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
      id: null,
      items: [
        { id: 0, title: 'Home', icon: 'mdi-home-variant-outline' },
        { id: 1, title: 'Inbox', icon: 'mdi-inbox' },
        { id: 2, title: 'Class', icon: 'mdi-video-box' },
        { id: 3, title: 'Students', icon: 'mdi-account-school' },
        { id: 4, title: 'Tests', icon: 'mdi-book-open-page-variant' },
        { id: 5, title: 'Files', icon: 'mdi-file-settings' },
        { id: 6, title: 'Settings', icon: 'mdi-cog' },
      ],
    }
  },
  methods: {
    setCurrentLinkId(id) {
      this.id = id
    },
  },
}
</script>

<style scoped>
.full-height {
  height: 100vh;
}

.link:hover {
  background: #efedfb;
}

.link-active {
  color: #5a58bd;
}

.spacer-box-1 {
  height: 2vh;
  width: 100%;
}
</style>
