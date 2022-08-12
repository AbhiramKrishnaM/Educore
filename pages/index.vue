<template>
  <v-container class="mt-5">
    <section class="grid-wrap">
      <HomeHeader class="grid-column-span-full" />
      <div class="box"></div>
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
  column-gap: 10px;
  row-gap: 10px;
  width: 100%;
}

.grid-column-span-full {
  grid-column: span 3;
}
</style>
