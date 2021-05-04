<template>
  <div
    class="w-64 bg-gray-900 rounded-r-lg text-gray-100 px-5 py-8 space-y-16 absolute inset-y-0 left-0 transform md:relative md:translate-x-0 transition duration-200 ease-in-out z-10"
    :class="{ '-translate-x-full': bool }"
  >
    <div class="flex justify-between px-4">
      <div class="flex items-center space-x-5">
        <div class="bg-gray-700 px-3 py-2 rounded-2xl">🚀</div>
        <span class="text-xl font-bold">LOGO</span>
      </div>
      <button class="focus:outline-none md:hidden" @click="closeMenu">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>
    </div>
    <nav class="space-y-4">
      <nuxt-link
        to="/admin/dashboard"
        class="flex items-center space-x-5 rounded transition duration-200 hover:bg-white hover:bg-opacity-20 hover:text-gray-100 hover:shadow-xl px-4 py-2.5"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
          />
        </svg>
        <span class="font-semibold text-md">Home</span>
      </nuxt-link>
      <nuxt-link
        to="/admin/users"
        class="flex items-center space-x-5 rounded transition duration-200 hover:bg-white hover:bg-opacity-20 hover:text-gray-100 hover:shadow-xl px-4 py-2.5"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"
          />
        </svg>
        <span class="font-semibold text-md">Users</span>
      </nuxt-link>
      <nuxt-link
        to="/admin/settings"
        class="flex items-center space-x-5 rounded transition duration-200 hover:bg-white hover:bg-opacity-20 hover:text-gray-100 hover:shadow-xl px-4 py-2.5"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"
          />
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
          />
        </svg>
        <span class="font-semibold text-md">Settings</span>
      </nuxt-link>
    </nav>
    <hr class="border-gray-700" />
    <div>
      <button
        class="w-full px-4 py-2.5 text-left text-white flex space-x-5 rounded transition duration-200 hover:bg-white hover:bg-opacity-20 hover:text-gray-100 hover:shadow-xl"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M11 16l-4-4m0 0l4-4m-4 4h14m-5 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h7a3 3 0 013 3v1"
          />
        </svg>
        <span>Log out</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bool: {
      type: Boolean,
      default: true,
      required: true,
    },
  },
  data() {
    return {}
  },
  watch: {
    $route() {
      this.closeMenu()
    },
  },
  methods: {
    closeMenu() {
      this.$emit('close')
    },
  },
}
</script>

<style scoped>
.nuxt-link-active {
  @apply bg-white;
  @apply bg-opacity-20;
  @apply text-gray-100;
  @apply shadow-xl;
}
</style>
