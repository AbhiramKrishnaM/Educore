<template>
  <div class="user-info-wrapper rounded-xl pa-6">
    <UiTeacherNameAndStatusCard :user-info="user">
      <template #user-name> Monica Howard </template>
      <template #user-avatar>
        <v-img :src="require('@/assets/images/classroom.png')" alt="John" />
      </template>
      <template #position> Maths Teacher </template>
    </UiTeacherNameAndStatusCard>

    <v-divider></v-divider>
  </div>
</template>
<script>
export default {
  name: 'HomeUserInfo',
  data() {
    return {
      user: {
        status: {
          isOnline: false,
        },
      },
    }
  },
}
</script>
<style scoped>
.user-info-wrapper {
  background-color: white;
}
</style>
