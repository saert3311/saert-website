<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
<script setup lang="ts">
useHead({
  titleTemplate: (pageTitle) => {
    return pageTitle
      ? `${pageTitle} - Jose Duarte`
      : 'Jose Duarte'
  }
})
const isOpen = useState('isOpen', () => false)
</script>
