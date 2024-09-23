<template><div>Content1</div></template>
<script setup lang="ts">
import { registerSW } from 'virtual:pwa-register'

const updateSW = registerSW({
  onNeedRefresh() {
    console.log('need refresh')
  },
  onOfflineReady() {}
})
</script>
<route lang="yaml">
meta:
  layout: layout
</route>
