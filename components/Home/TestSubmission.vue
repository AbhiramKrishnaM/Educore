<template>
  <div class="wrapper rounded-xl pa-6">
    <UiComponentNav :option-class-drop-down="true">
      <template #title>
        <h1>Submitted Tests</h1>
      </template>
    </UiComponentNav>
    <UiTable />
  </div>
</template>
<script>
export default {
  name: 'HomeTestSubmission',
  data() {
    return {
      items: [
        { title: 'Class 7th' },
        { title: 'Class 8th' },
        { title: 'Class 9th' },
        { title: 'Class 10th' },
      ],
    }
  },
}
</script>
<style scoped>
.wrapper {
  background: #fff;
}
</style>
