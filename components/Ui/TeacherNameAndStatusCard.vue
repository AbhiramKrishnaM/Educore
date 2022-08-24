<template>
  <div class="teacher-name-status-wrapper d-flex align-center mb-3">
    <v-avatar size="56">
      <v-slot name="user-avatar">
        <v-img :src="require('@/assets/images/classroom.png')" alt="John" />
      </v-slot>
    </v-avatar>
    <div class="ml-3">
      <div class="text-subtitle-1 font-weight-bold">
        <slot name="user-name">Monica Howard</slot>
      </div>

      <div class="text-body-2 grey--text font-weight-bold">
        <slot name="position">Maths Teacher</slot>
      </div>
    </div>
    <div v-if="userInfo.status.isOnline" class="status d-flex align-center">
      <div class="success mr-1 small-dot"></div>
      <div class="success--text text-caption font-weight-bold">Online</div>
    </div>

    <div v-else class="status d-flex align-center">
      <div class="error mr-1 small-dot"></div>
      <div class="error--text text-caption font-weight-bold">Offline</div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'TeacherNameAndStatusCardUI',
  props: { userInfo: { type: Object, required: true } },
}
</script>

<style scoped>
.teacher-name-status-wrapper {
  position: relative;
}

.status {
  position: absolute;
  right: 20px;
  top: 0;
}

.small-dot {
  width: 8px;
  height: 8px;
  border-radius: 100%;
}
</style>
