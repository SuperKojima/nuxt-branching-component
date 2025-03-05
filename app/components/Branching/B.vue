<script setup lang="ts">
import type { Classification } from './type'

const props = defineProps<{
  classification: Classification
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
