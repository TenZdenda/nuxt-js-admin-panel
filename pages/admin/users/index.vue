<template>
  <div>
    <div class="mb-10 flex items-center justify-between">
      <div>
        <h1 class="text-2xl font-bold">Manage your users</h1>
        <p class="text-gray-500">Create, edit or just delete them</p>
      </div>
      <div>
        <nuxt-link
          to="users/new"
          class="focus:outline-none text-gray-500 hover:text-gray-900"
        >
          <div class="flex items-center gap-5">
            <p class="font-semibold">Create new user</p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 8l4 4m0 0l-4 4m4-4H3"
              />
            </svg>
          </div>
        </nuxt-link>
      </div>
    </div>

    <Table />
  </div>
</template>

<script>
export default {
  layout: 'admin',
}
</script>
