<template>
  <div>
    <slot :chip="chipType">
      <v-chip v-if="chipType === 'active'" color="#ECECFB" class="purple--text">
        Active
      </v-chip>

      <v-chip v-if="chipType === 'opened'" color="#FAF0E4" class="orange--text">
        Opened
      </v-chip>

      <v-chip v-if="chipType === 'completed'" color="#FEEBEB" class="red--text">
        Completed
      </v-chip>
    </slot>
  </div>
</template>
<script>
export default {
  name: 'ChipUI',
  data() {
    return {
      chipType: null,
    }
  },
}
</script>
