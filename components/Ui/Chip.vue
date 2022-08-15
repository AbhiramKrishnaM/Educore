<template>
  <div>
    <v-chip v-if="chipType === 'active'" color="#ECECFB" class="purple--text">
      Active
    </v-chip>

    <v-chip v-if="chipType === 'opened'" color="#FAF0E4" class="orange--text">
      Opened
    </v-chip>

    <v-chip v-if="chipType === 'completed'" color="#FEEBEB" class="red--text">
      Completed
    </v-chip>
  </div>
</template>
<script>
export default {
  name: 'ChipUI',
  props: { chipType: { type: String, required: true } },
}
</script>
