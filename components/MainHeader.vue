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
        <button
          @click="toggleState"
          class="menu-btn text-gray-500 hover:text-gray-800"
        >
          <svg
            v-if="isOpen"
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
              clip-rule="evenodd"
            />
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>
        </button>
      </div>
    </div>
    <Navigation />
  </header>
</template>
<script setup>
const isOpen = useState('isOpen')

const toggleState = () => {
    isOpen.value = !isOpen.value
}
</script>