<template>
  <v-app>
    <!-- navigation bar -->

    <v-navigation-drawer
      v-model="drawer"
      :permanent="$vuetify.breakpoint.mdAndUp"
      app
    >
      <div class="wrapper d-flex flex-column">
        <v-list flat dense nav class="mb-2">
          <v-list-item link :ripple="false">
            <v-list-item-icon class="mr-4">
              <v-img
                height="30"
                width="30"
                contain
                :src="require('@/assets/images/logo.svg')"
              ></v-img>

              <div
                class="ml-3 text-subtitle-1 font-weight-bold blue-grey-text text-darken-4 logo-txt-color"
                v-text="'EduCore'"
              ></div>
            </v-list-item-icon>
          </v-list-item>
        </v-list>

        <v-list flat dense nav>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            :ripple="false"
            :input-value="id === item.id"
            active-class="link-active"
            link
            class="link"
            :to="item.to"
            @click="setCurrentLinkId(item.id)"
          >
            <v-list-item-icon class="mr-4">
              <v-icon :class="id === item.id ? '' : 'grey-color'">{{
                item.icon
              }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title :class="id === item.id ? '' : 'grey-color'">{{
                item.title
              }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <v-list class="mt-auto">
          <v-list-item>
            <v-list-item-content>
              <LayoutsClass />
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </div>
    </v-navigation-drawer>
    <!-- app bar -->
    <v-app-bar absolute color="transparent" app flat class="px-3">
      <v-app-bar-nav-icon
        class="d-md-none"
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>

      <v-spacer class="d-md-none"></v-spacer>
      <v-toolbar-title
        :class="{
          'text-h5': $vuetify.breakpoint.smAndDown,
          'text-h4': $vuetify.breakpoint.mdAndUp,
        }"
        class="font-weight-medium"
        >Good Morning, Monica ????</v-toolbar-title
      >

      <v-spacer></v-spacer>

      <v-btn depressed min-width="20" class="rounded-lg">
        <v-icon color="#858283">mdi-bell-outline</v-icon>
      </v-btn>
    </v-app-bar>

    <!--  -->
    <v-main>
      <Nuxt />
    </v-main>
    <!--  -->
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',

  data() {
    return {
      id: 0,
      drawer: false,
      items: [
        { id: 0, title: 'Home', icon: 'mdi-home-variant-outline', to: '/' },
        { id: 1, title: 'Inbox', icon: 'mdi-inbox', to: '/inbox' },
        { id: 2, title: 'Class', icon: 'mdi-video-box', to: '/class' },
        {
          id: 3,
          title: 'Students',
          icon: 'mdi-account-school',
          to: '/students',
        },
        {
          id: 4,
          title: 'Tests',
          icon: 'mdi-book-open-page-variant',
          to: '/tests',
        },
        { id: 5, title: 'Files', icon: 'mdi-file-settings', to: '/files' },
        { id: 6, title: 'Settings', icon: 'mdi-cog', to: '/settings' },
      ],
    }
  },

  computed: {
    mobile() {
      return !this.$vuetify.breakpoint.smAndDown
    },
  },

  methods: {
    setCurrentLinkId(id) {
      this.id = id
    },
  },
}
</script>

<style scoped>
.grey-color {
  color: #cbcbcb;
}

.wrapper {
  height: 100%;
}

.logo-txt-color {
  color: #2a2b50;
}

.link:hover {
  background: #efedfb;
}

.link-active {
  color: #5a58bd;
}
</style>
