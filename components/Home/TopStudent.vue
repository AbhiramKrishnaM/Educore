<template>
  <div class="wrapper rounded-xl pa-6">
    <UiComponentNav :option-class-drop-down="true">
      <template #title>
        <h1>Top student</h1>
      </template>
    </UiComponentNav>

    <div>
      <UiTopStudent
        v-for="(student, index) in topStudents"
        :key="index"
        :percentage="student.percentage"
      >
        <template #student-avatar>
          <v-img :src="student.student_details.avatar" alt="avatar"></v-img>
        </template>
        <template #student-name>
          {{ student.student_details.student_name }}
        </template>
        <template #percentage>
          {{ student.percentage + '%' }}
        </template>
      </UiTopStudent>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeTopStudent',
  data() {
    return {
      topStudents: [
        {
          id: 0,
          percentage: 80,
          student_details: {
            student_name: 'Abhiram krishna',
            avatar:
              'https://cdn.pixabay.com/photo/2021/11/12/03/04/woman-6787784_960_720.png',
          },
        },
        {
          id: 1,
          percentage: 70,
          student_details: {
            student_name: 'Hari',
            avatar:
              'https://cdn.pixabay.com/photo/2016/03/31/19/58/avatar-1295429_960_720.png',
          },
        },
        {
          id: 2,
          percentage: 90,
          student_details: {
            student_name: 'Fahid Hassan',
            avatar:
              'https://cdn.pixabay.com/photo/2020/11/22/22/17/male-5768177_960_720.png',
          },
        },
      ],
    }
  },
}
</script>
<style scoped>
.wrapper {
  background-color: #fff;
}
</style>
