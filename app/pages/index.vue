<script setup lang="ts">
const route = useRoute()
const municipality = route.query.municipality
const classification = route.query.classification

if (!municipality || !classification) {
  throw createError({
    statusCode: 400,
    statusMessage: 'Bad Request',
  })
}
</script>

<template>
  <div>
    <Branching municipality="A" classification="X" />
  </div>
</template>
