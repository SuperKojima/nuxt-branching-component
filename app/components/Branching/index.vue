<script setup lang="ts">
import BranchingB from './B.vue'
import BranchingC from './C.vue'
import BranchingDefault from './Default.vue'

const props = defineProps<{
  municipality: 'A' | 'B' | 'C'
  classification?: 'X' | 'Y' | 'Z'
}>()

function getComponent() {
  switch (props.classification) {
    case 'B':
      return BranchingB
    case 'C':
      return BranchingC
    default:
      return BranchingDefault
  }
}
</script>

<template>
  <component :is="getComponent()" :classification="props.classification" />
</template>
