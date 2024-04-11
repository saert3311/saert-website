<template>
        <nav
      :class="{
        'absolute top-0 inset-x-0 bg-white shadow-lg rounded-xl border mx-2 mt-2 md:shadow-none md:border-none md:mx-0 md:mt-0 md:relative md:bg-transparent':
        isOpen,
      }"
      class="pb-5 md:text-sm"
    >
      <div
        class="gap-x-14 items-center max-w-screen-xl mx-auto px-4 md:flex md:px-8"
      >
        <!-- Logo and Menu Toggle Button - Desktop View -->
        <div class="flex items-center justify-between py-5 md:block">
          <NuxtLink to="/">
            <div class="flex items-center">
                <MainLogo />
                <h3 class="text-xl text-gray-800 font-bold sm:text-2xl ml-2">Jose Duarte</h3>
            </div>
          </NuxtLink>
          <div class="md:hidden">
            <MenuButton />
          </div>
        </div>
        <!-- Navigation Links -->
        <div
          :class="{ block: isOpen, hidden: !isOpen }"
          class="flex-1 items-center mt-8 md:mt-0 md:flex"
        >
          <ul
            class="flex-1 justify-center items-center space-y-6 md:flex md:space-x-6 md:space-y-0"
          >
            <li
              v-for="item in menuItems"
              :key="item.title"
              class="text-gray-700 hover:text-gray-900"
            >
              <NuxtLink :to="item.path" class="block">{{ item.title }}</NuxtLink>
            </li>
          </ul>
          <div class="items-center justify-end mt-6 space-y-6 md:flex md:mt-0">
            <a
              href="javascript:void(0)"
              class="flex items-center justify-center gap-x-1 py-2 px-4 text-white font-medium bg-gray-800 hover:bg-gray-700 active:bg-gray-900 rounded-full md:inline-flex"
            >
              Contacto
              <IconsRightArrow />
            </a>
          </div>
        </div>
      </div>
    </nav>
</template>
<script setup>
const menuItems = [
  { title: 'El Blog', path: '/blog' },
  { title: 'Portafolio', path: '/portafolio' },
]

const isOpen = useState('isOpen')

</script>