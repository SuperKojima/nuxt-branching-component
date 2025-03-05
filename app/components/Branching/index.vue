<script setup lang="ts">
import type { Classification, Municipality } from './type'
import BranchingB from './B.vue'
import BranchingC from './C.vue'
import BranchingDefault from './Default.vue'

const props = defineProps<{
  municipality: Municipality
  classification: Classification
}>()

function getComponent() {
  switch (props.municipality) {
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
