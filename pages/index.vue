<template>
  <v-container fluid class="mt-5">
    <section
      class="grid-wrap px-3"
      :class="{ 'height-at-sm-and-down': $vuetify.breakpoint.smAndDown }"
    >
      <HomeHeader
        :class="{
          'grid-column-span-3': $vuetify.breakpoint.mdAndUp,
          'grid-column-span-full': $vuetify.breakpoint.smAndDown,
        }"
      />
      <HomeUserInfo
        :class="{
          'grid-column-span-1 grid-row-span-5': $vuetify.breakpoint.mdAndUp,
          'grid-column-span-full  ': $vuetify.breakpoint.smAndDown,
        }"
      />

      <HomeTestSubmission
        :class="{
          'grid-column-span-3 grid-row-span-2': $vuetify.breakpoint.mdAndUp,
          'grid-column-span-full': $vuetify.breakpoint.smAndDown,
        }"
      />

      <HomeTopStudent
        :class="{
          'grid-column-span-1 grid-row-span-2': $vuetify.breakpoint.mdAndUp,
          'grid-column-span-2': $vuetify.breakpoint.smAndDown,
        }"
      />

      <HomeGroups
        :class="{
          'grid-column-span-2 grid-row-span-2': $vuetify.breakpoint.mdAndUp,
          'grid-column-span-2': $vuetify.breakpoint.smAndDown,
        }"
      />
    </section>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style scoped>
.box {
  width: 100%;
  height: 100%;
  background-color: grey;
}

.height-at-sm-and-down {
  height: 100vh;
}

.grid-wrap {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(5, 0.8fr);
  gap: 10px;
  width: 100%;
}

.grid-column-span-1 {
  grid-column: span 1;
}

.grid-column-span-2 {
  grid-column: span 2;
}

.grid-column-span-3 {
  grid-column: span 3;
}

.grid-column-span-full {
  grid-column: span 4;
}

.grid-row-span-1 {
  grid-row: span 1;
}

.grid-row-span-2 {
  grid-row: span 2;
}

.grid-row-span-5 {
  grid-row: span 5;
}

.grid-row-3-2 {
  grid-row: 3 / span 2;
}
</style>
