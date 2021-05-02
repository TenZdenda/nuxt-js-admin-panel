<template>
  <div class="w-full h-auto border border-gray-100 rounded">
    <div class="p-10">
      <h2 class="text-gray-600 text-xl">{{ name }}</h2>
      <p class="text-4xl font-bold my-4">{{ record }}</p>
      <div class="flex items-center">
        <div
          class="p-1 rounded-full"
          :class="[
            dup ? 'bg-green-100 text-green-500' : 'bg-red-100 text-red-500',
          ]"
        >
          <svg
            v-if="dup"
            xmlns="http://www.w3.org/2000/svg"
            class="h-4 w-4"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"
            />
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            class="h-4 w-4"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M13 17h8m0 0V9m0 8l-8-8-4 4-6-6"
            />
          </svg>
        </div>
        <p class="ml-2 text-gray-400">
          <span
            class="font-bold"
            :class="[dup ? 'text-green-500' : 'text-red-500']"
            ><span v-if="dup">+</span> {{ dpercent }} %</span
          >
          vs last month
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    record: {
      type: String,
      required: true,
    },
    dup: {
      type: Boolean,
      required: true,
    },
    dpercent: {
      type: Number,
      required: true,
    },
  },
}
</script>
