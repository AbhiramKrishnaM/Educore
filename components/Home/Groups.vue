<template>
  <div class="wrapper rounded-xl pa-6">
    <UiComponentNav :option-view-all="true">
      <template #title>
        <h1>Groups</h1>
      </template>
    </UiComponentNav>
  </div>
</template>
<script>
export default {
  name: 'HomeGroups',
}
</script>
<style scoped>
.wrapper {
  background: #fff;
}
</style>
