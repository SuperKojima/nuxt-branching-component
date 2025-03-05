<script setup lang="ts">
const props = defineProps<{
  classification: 'X' | 'Y' | 'Z'
}>()
</script>

<template>
  <div>
    <div>
      B.vue
    </div>
    <div>
      {{ props.classification }}
    </div>
  </div>
</template>
