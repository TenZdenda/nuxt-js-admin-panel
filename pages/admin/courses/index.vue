<template>
  <div>
    <div class="mb-10 flex items-center justify-between">
      <div>
        <h1 class="text-3xl font-bold">Courses</h1>
      </div>
      <div>
        <nuxt-link
          to="/admin/courses/new"
          class="focus:outline-none text-gray-500 hover:text-gray-900"
        >
          <div class="flex items-center gap-5">
            <p class="font-semibold">Create new courses</p>
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

    <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
      <div
        class="w-full h-48 bg-gradient-to-br from-purple-500 to-indigo-500 rounded-2xl flex"
      >
        <div class="m-auto">
          <span class="font-bold text-white text-xl">Courses 1</span>
        </div>
      </div>
      <div
        class="w-full h-48 bg-gradient-to-br from-green-400 to-blue-500 rounded-2xl flex"
      >
        <div class="m-auto">
          <span class="font-bold text-white text-xl">Courses 1</span>
        </div>
      </div>
      <div
        class="w-full h-48 bg-gradient-to-br from-purple-400 via-pink-500 to-red-500 rounded-2xl flex"
      >
        <div class="m-auto">
          <span class="font-bold text-white text-xl">Courses 1</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'admin',
  data() {
    return {
      thead: ['Name', 'E-mail', 'Phone'],
      data: [
        [
          {
            id: 10,
            image: 'https://avatars.githubusercontent.com/u/39481226?v=4',
            text: 'Zdeněk Pašek',
          },
          {
            text: 'hello@zdenekpasek.com',
          },
          {
            text: '+45 11 22 33 44',
          },
        ],
        [
          {
            id: 11,
            image:
              'https://images.unsplash.com/photo-1531427186611-ecfd6d936c79?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=934&q=30',
            text: 'John Doe',
          },
          {
            text: 'johndoe@example.com',
          },
          {
            text: '+420 111 333 444',
          },
        ],
      ],
    }
  },
  methods: {
    deleteItem(item) {
      console.log(item)
    },
    editItem(item) {
      console.log(item)
    },
  },
}
</script>
