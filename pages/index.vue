<template>
  <v-container class="mt-5">
    <section class="grid-wrap">
      <HomeHeader class="grid-column-span-3" />
      <HomeUserInfo class="grid-column-span-1 grid-row-span-5" />

      <HomeTestSubmission class="grid-column-span-3 grid-row-span-2" />

      <HomeTopStudent class="grid-column-span-1 grid-row-span-2" />

      <HomeGroups class="grid-column-span-2 grid-row-span-2" />
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

.grid-row-span-2 {
  grid-row: span 2;
}

.grid-row-span-5 {
  grid-row: span 5;
}
</style>
