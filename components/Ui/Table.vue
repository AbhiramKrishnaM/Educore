<template>
  <div class="wrapper pa-3">
    <v-row no-gutters class="head rounded-tr-lg rounded-tl-lg">
      <v-col sm="3" class="border-right px-3 py-2"> <h1>Name</h1> </v-col>
      <v-col sm="4" class="border-right px-3 py-2"
        ><h1>Date Of Submission</h1></v-col
      >
      <v-col sm="3" class="border-right px-3 py-2"><h1>Status</h1></v-col>
      <v-col sm="1" class="border-right px-3 py-2"></v-col>
      <v-col sm="1"></v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  name: 'TableUI',
}
</script>
<style scoped>
.border-right {
  border-right: 1px solid #ececec;
}

.wrapper {
  background: transparent;
}

.head {
  /* background: #f8f9fd; */
  border: 1px solid #ececec;
}

h1 {
  font-size: 18px;
}
</style>
