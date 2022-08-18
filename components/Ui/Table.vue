<template>
  <div class="wrapper pt-3">
    <v-row no-gutters class="head rounded-tr-lg rounded-tl-lg">
      <v-col sm="3" class="border-right px-3 py-2"> <h1>Name</h1> </v-col>
      <v-col sm="4" class="border-right px-3 py-2"
        ><h1>Date Of Submission</h1></v-col
      >
      <v-col sm="3" class="border-right px-3 py-2"><h1>Status</h1></v-col>
      <v-col sm="1" class="border-right px-3 py-2"></v-col>
      <v-col sm="1"></v-col>
    </v-row>
    <div class="table-body-wrapper">
      <UiTableBody
        v-for="(submission, index) in studentSubmissions"
        :key="index"
        :submission-array-length="studentSubmissions.length"
        :item-index="index"
        :status="submission.status"
      >
        <template #studentAvatar>
          <v-img :src="submission.student_details.avatar" alt="avatar"></v-img>
        </template>
        <template #studentName> {{ submission.student_name }} </template>
        <template #deadline>{{ submission.submission_date }}</template>
      </UiTableBody>
    </div>
  </div>
</template>
<script>
export default {
  name: 'TableUI',
  data() {
    return {
      studentSubmissions: [
        {
          id: 0,
          student_name: 'Abhiram krishna',
          submission_date: 'December 17, 2021',
          status: 'opened',
          student_details: {
            avatar:
              'https://cdn.pixabay.com/photo/2021/11/12/03/04/woman-6787784_960_720.png',
          },
        },
        {
          id: 2,
          student_name: 'Hari',
          submission_date: 'March 22, 2021',
          status: 'active',
          student_details: {
            avatar:
              'https://cdn.pixabay.com/photo/2016/03/31/19/58/avatar-1295429_960_720.png',
          },
        },
        {
          id: 3,
          student_name: 'Fahid Hassan',
          submission_date: 'January 1, 2021',
          status: 'completed',
          student_details: {
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
.border-right {
  border-right: 1px solid #ececec;
}

.wrapper {
  background: transparent;
}

.head {
  background: #f8f9fd;
  border: 1px solid #ececec;
}

h1 {
  font-size: 18px;
  color: #4a5258;
}

.table-body-wrapper {
  min-height: max-content;
  max-height: 20vh;
  overflow-y: scroll;
}
</style>
