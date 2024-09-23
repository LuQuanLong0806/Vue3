<template>
  <div>vite-plugin-pages</div>
  <div>
    {{ msg }}
  </div>
  <HelloWorld></HelloWorld>
  <div ref="target">
    <h1>Hello world</h1>
  </div>
  <p>x:{{ x }}</p>
  <p>y:{{ y }}</p>
  <p>isOutside:{{ isOutside }}</p>
  <TestComponent></TestComponent>
</template>

<script setup lang="ts">
const msg = ref('111s')
const target = ref(null)
const { x, y, isOutside } = useMouseInElement(target)
</script>
<style scoped></style>
<route lang="yaml">
meta:
  layout: layout
</route>
