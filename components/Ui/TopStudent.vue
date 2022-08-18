<template>
  <div class="wrapper mt-4 pa-2 rounded-lg d-flex align-center shadow-default">
    <div class="flex-item d-flex align-center">
      <v-avatar size="50" class="mr-2">
        <slot name="student-avatar">
          <v-img :src="require('@/assets/images/placeholder.png')"></v-img>
        </slot>
      </v-avatar>

      <div>
        <div class="font-weight-medium text-h6">
          <slot name="student-name">Lucas Jones</slot>
        </div>
        <div class="error--text text-body-2">
          Allover score: <slot name="percentage">100%</slot>
        </div>
      </div>
    </div>

    <v-img
      v-if="percentage >= 90"
      height="50"
      contain
      :src="require('@/assets/images/marks/crown.svg')"
    ></v-img>
    <v-img
      v-if="percentage >= 80 && percentage < 90"
      height="50"
      contain
      :src="require('@/assets/images/marks/fern.svg')"
    ></v-img>
    <v-img
      v-if="percentage >= 70 && percentage < 80"
      height="50"
      contain
      :src="require('@/assets/images/marks/cup.svg')"
    ></v-img>
  </div>
</template>
<script>
export default {
  name: 'TopStudentUI',
  props: { percentage: { type: Number, required: true } },
}
</script>

<style scoped>
.wrapper {
  background-color: #f9f8fd;
}

.shadow-default {
  box-shadow: 3px 3px #a09178;
}

.shadow-default:hover {
  box-shadow: none;
}

.flex-item {
  flex: 7;
}
</style>
