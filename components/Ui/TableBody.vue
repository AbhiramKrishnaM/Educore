<template>
  <v-row
    no-gutters
    class="body"
    :class="{
      'rounded-br-lg rounded-bl-lg': itemIndex === submissionArrayLength - 1,
    }"
  >
    <v-col sm="3" class="border-right px-3 py-2">
      <h1>
        <v-avatar size="35" class="mr-2">
          <slot name="studentAvatar">
            <v-img :src="require('@/assets/images/placeholder.png')"></v-img>
          </slot>
        </v-avatar>
        <slot name="studentName"> Name </slot>
      </h1>
    </v-col>
    <v-col sm="4" class="border-right px-3 py-3">
      <span> <slot name="deadline">Date Of Submission</slot></span>
    </v-col>
    <v-col sm="3" class="border-right px-3 py-2">
      <UiChip :chip-type="status" />
    </v-col>
    <v-col sm="1" class="border-right px-3 py-2">
      <v-btn icon plain> <v-icon color="success">mdi-download</v-icon></v-btn>
    </v-col>
    <v-col sm="1" class="px-3 py-2">
      <v-btn icon plain @click="isViewed = !isViewed">
        <v-icon>{{
          isViewed ? 'mdi-eye-off-outline' : 'mdi-eye-outline'
        }}</v-icon></v-btn
      >
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: 'TableBodyUI',
  props: {
    submissionArrayLength: { type: Number, required: true },
    itemIndex: { type: Number, required: true },
    status: { type: String, required: true, default: 'active' },
  },
  data() {
    return {
      isViewed: false,
      chip: 'completed',
    }
  },
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

span {
  font-size: 15px;
  font-weight: 500;
  color: #c2c2c2;
}
</style>
