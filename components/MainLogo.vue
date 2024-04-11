<template>
  <svg
    version="1.1"
    id="Capa_1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    x="0px"
    y="0px"
    viewBox="0 0 792.43 662.95"
    style="enable-background: new 0 0 792.43 662.95"
    xml:space="preserve"
    :width="props.width"
    :height="props.height"
  >
    <g>
      <polygon class="st0" points="227.85,311.65 26.36,647.15 441.02,443.87 	" />
      <polygon
        class="st1"
        points="772.93,647.15 599.33,362.92 441.02,443.87 	"
      />
      <polygon
        class="st2"
        points="399.65,22.01 227.85,311.65 441.02,443.87 599.33,362.92 	"
      />
    </g>
  </svg>
</template>
<script setup>
const props = defineProps({
  width: {
    type: Number,
    default: 50,
  },
  height: {
    type: Number,
    default: 50,
  },
})
</script>
<style>
.st0 {
  fill: #e2e242;
}
.st1 {
  fill: #c62a9a;
}
.st2 {
  fill: #69e3ff;
}
</style>