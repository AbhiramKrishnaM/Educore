<template>
  <v-row no-gutters class="body">
    <v-col sm="3" class="border-right px-3 py-2">
      <h1>
        <v-avatar size="35" class="mr-2">
          <slot name="avatar">
            <v-img :src="require('@/assets/images/placeholder.png')"></v-img>
          </slot> </v-avatar
        >Name
      </h1>
    </v-col>
    <v-col sm="4" class="border-right px-3 py-2"
      ><h1>Date Of Submission</h1></v-col
    >
    <v-col sm="3" class="border-right px-3 py-2"><h1>Status</h1></v-col>
    <v-col sm="1" class="border-right px-3 py-2"></v-col>
    <v-col sm="1"></v-col>
  </v-row>
</template>
<script>
export default {
  name: 'TableBodyUI',
}
</script>
<style scoped>
.body {
  border: 1px solid #ececec;
}

.border-right {
  border-right: 1px solid #ececec;
}

h1 {
  font-size: 18px;
  color: #4a5258;
}
</style>
