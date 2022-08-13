<template>
  <div class="wrapper rounded-xl pa-6">
    <div class="d-flex justify-space-between">
      <h1>Submitted Tests</h1>
      <span
        >Class 6th

        <v-menu
          transition="slide-x-transition"
          nudge-left="60"
          nudge-bottom="10"
          bottom
          offset-y
        >
          <template #activator="{ on, attrs }">
            <v-btn plain icon
              ><v-icon color="#C2C2C2" v-bind="attrs" v-on="on"
                >mdi-chevron-down</v-icon
              ></v-btn
            >
          </template>

          <v-list>
            <v-list-item v-for="(item, index) in items" :key="index">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeTestSubmission',
  data() {
    return {
      items: [
        { title: 'Class 7th' },
        { title: 'Class 8th' },
        { title: 'Class 9th' },
        { title: 'Class 10th' },
      ],
    }
  },
}
</script>
<style scoped>
.wrapper {
  background: #fff;
}

span {
  font-weight: bold;
  color: #c2c2c2;
}
</style>
