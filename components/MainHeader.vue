<template>
  <header>
    <div :class="{ 'mx-2 pb-5': isOpen, hidden: !isOpen }" class="md:hidden">
      <div class="flex items-center justify-between py-5 md:block">
        <a href="javascript:void(0)">
          <img
            src="https://www.floatui.com/logo.svg"
            width="120"
            height="50"
            alt="Float UI logo"
          />
        </a>
        <MenuButton />
      </div>
    </div>
    <Navigation />
  </header>
</template>
<script setup>
const isOpen = useState('isOpen')
</script>