<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <n-message-provider>
    <RouterView />
  </n-message-provider>
</template>

<style scoped></style>
