<template>
  <v-badge
    :value="newNotificationCount"
    color="green"
    :content="'+' + newNotificationCount"
    offset-x="20"
    offset-y="30"
  >
    <div class="wrapper mt-4 pa-2 rounded-lg d-flex align-center">
      <v-avatar rounded size="70" class="mr-2">
        <slot name="group-avatar">
          <v-img :src="require('@/assets/images/dummy-group.jpg')"></v-img>
        </slot>
      </v-avatar>

      <div class="ml-3">
        <div class="font-weight-bold text-subtitle-1">
          <slot name="title">Teacher's Group</slot>
        </div>
        <div class="font-weight-light text-subtitle-2">
          <slot name="info"> wade warren i'm facing an issue </slot>
        </div>
      </div>
    </div>
  </v-badge>
</template>
<script>
export default {
  name: 'GroupCardUI',
  props: { newNotificationCount: { type: Number, default: 0 } },
}
</script>

<style scoped>
.wrapper {
  background-color: #f9f8fd;
}
</style>
