<template>
  <div class="wrapper rounded-xl pa-6">
    <UiComponentNav :option-view-all="true">
      <template #title>
        <h1>Groups</h1>
      </template>
    </UiComponentNav>

    <div class="d-flex flex-column minimum-height pa-2">
      <UiGroupCard v-for="(group, index) in groups" :key="index">
        <template #group-avatar>
          <v-img :src="group.group_info.avatar" alt="group avatar"></v-img>
        </template>

        <template #title>{{ group.title }}</template>
        <template #info>{{ group.info }}</template>
      </UiGroupCard>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeGroups',
  data() {
    return {
      groups: [
        {
          id: 0,
          title: 'helooooo',
          info: 'go concept released',
          group_info: {
            avatar:
              'https://images.pexels.com/photos/1703314/pexels-photo-1703314.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
          },
        },
        {
          id: 1,
          title: "Teacher's group",
          info: 'hello i love javascript and i like to code',
          group_info: {
            avatar:
              'https://images.pexels.com/photos/1000445/pexels-photo-1000445.jpeg?cs=srgb&dl=pexels-belle-co-1000445.jpg&fm=jpg',
          },
        },
      ],
    }
  },
}
</script>
<style scoped>
.wrapper {
  background: #fff;
}

.minimum-height {
  height: 30vh;
  overflow-y: scroll;
}
</style>
