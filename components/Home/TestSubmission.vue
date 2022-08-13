<template>
  <div class="wrapper rounded-xl pa-6">
    <div class="d-flex justify-space-between">
      <h1>Submitted Tests</h1>
      <span
        >Class 6th
        <v-btn icon
          ><v-icon color="#DBDBDB">mdi-chevron-down</v-icon></v-btn
        ></span
      >
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeTestSubmission',
}
</script>
<style scoped>
.wrapper {
  background: #fff;
}

span {
  font-weight: bold;
  color: #dbdbdb;
}
</style>
