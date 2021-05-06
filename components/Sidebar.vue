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
            d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4"
          />
        </svg>
        <span class="font-semibold text-md">Dashboard</span>
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
          <path d="M12 14l9-5-9-5-9 5 9 5z" />
          <path
            d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"
          />
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222"
          />
        </svg>
        <span class="font-semibold text-md">Students</span>
      </nuxt-link>
      <nuxt-link
        to="/admin/courses"
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
            d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01"
          />
        </svg>
        <span class="font-semibold text-md">Courses</span>
      </nuxt-link>
      <nuxt-link
        to="/admin/staff"
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
        <span class="font-semibold text-md">Staff</span>
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
        class="w-full px-4 py-2.5 text-left text-white flex space-x-5 rounded transition duration-200 hover:bg-white hover:bg-opacity-20 hover:text-gray-100 hover:shadow-xl focus:outline-none"
        @click="logout"
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
    logout() {
      console.log('logout click')
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
