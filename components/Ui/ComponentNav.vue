<template>
  <div class="wrapper d-flex justify-space-between">
    <slot name="title">
      <h1>Enter some title</h1>
    </slot>

    <span v-show="optionClassDropDown"
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

    <span v-show="optionViewAll">
      View All
      <v-btn plain icon
        ><v-icon color="#C2C2C2">mdi-chevron-right</v-icon></v-btn
      >
    </span>
  </div>
</template>
<script>
export default {
  name: 'ComponentNavUI',
  props: {
    optionClassDropDown: { type: Boolean, default: false },
    optionViewAll: { type: Boolean, default: false },
  },

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
span {
  font-weight: bold;
  color: #c2c2c2;
}
</style>
