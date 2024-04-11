<template>
  <header>
    <div :class="{ 'mx-2 pb-5': isOpen, hidden: !isOpen }" class="md:hidden">
      <div class="flex items-center justify-between py-5 md:block">
        <NuxtLink to="/">
            <MainLogo />
        </NuxtLink>
        <MenuButton />
      </div>
    </div>
    <Navigation />
  </header>
</template>
<script setup>
const isOpen = useState('isOpen')
</script>