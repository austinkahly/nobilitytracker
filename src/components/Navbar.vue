<template>
<nav class="bg-purple-900">
  <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
    <div class="relative flex items-center justify-between h-16">
      <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
        <!-- Mobile menu button-->
        <button type="button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-purple-600 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" aria-controls="mobile-menu" aria-expanded="false">
          <span class="sr-only">Open main menu</span>

          <svg class="h-6 w-6" v-if="!hamburger" @click.prevent="toggleHamburger" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
          <svg class="h-6 w-6" v-if="hamburger" @click.prevent="toggleHamburger"  xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
        <div class="flex-shrink-0 flex items-center">
          <a href="https://nobilitytracker.com"><img class="h-12 w-auto" src="@/assets/logo.svg" alt="Workflow"></a>
        </div>
        <div class="hidden sm:flex sm:ml-6 items-center">
          <div class="flex space-x-4">
            <a href="https://nobilitytoken.com/" target="_blank" class="text-gray-300 hover:bg-purple-600 hover:text-white px-3 py-2 rounded-md text-sm font-medium">Nobility Website</a>
            <a href="https://twitter.com/ThePatrity" target="_blank" class="text-gray-300 hover:bg-purple-600 hover:text-white px-3 py-2 rounded-md text-sm font-medium">Twitter</a>
            <a href="https://github.com/Yoters/nobilitytracker" target="_blank" class="text-gray-300 hover:bg-purple-600 hover:text-white px-3 py-2 rounded-md text-sm font-medium">Source Code</a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Mobile menu, show/hide based on menu state. -->
  <div class="sm:hidden" id="mobile-menu" v-if="hamburger">
    <div class="px-2 pt-2 pb-3 space-y-1">
      <a href="https://nobilitytoken.com/" target="_blank" class="text-gray-300 hover:bg-purple-600 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Nobility Website</a>
      <a href="https://twitter.com/ThePatrity" target="_blank" class="text-gray-300 hover:bg-purple-600 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Twitter</a>
      <a href="https://github.com/Yoters/nobilitytracker" target="_blank" class="text-gray-300 hover:bg-purple-600 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Source Code</a>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  data() {
    return {
      hamburger: false,
    }
  },
  methods: {
    toggleHamburger() {
      this.hamburger = !this.hamburger
    }
  }
}
</script>

<style scoped>

</style>
