<template>
  <div class="flex flex-col">
    <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
      <div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8">
        <div class="overflow-hidden border-b border-gray-200 rounded">
          <table class="min-w-full divide-y divide-gray-200">
            <thead class="bg-gray-50">
              <tr>
                <th
                  v-for="item in thead"
                  :key="item"
                  scope="col"
                  class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
                >
                  {{ item }}
                </th>
                <th v-if="updates" scope="col" class="relative px-6 py-3">
                  <span class="sr-only">Action</span>
                </th>
              </tr>
            </thead>
            <tbody
              v-for="(tbody, index) in data"
              :key="index"
              class="bg-white divide-y divide-gray-200"
            >
              <tr>
                <td
                  v-for="item in tbody"
                  :key="item.text"
                  class="px-6 py-4 whitespace-nowrap"
                >
                  <div class="flex items-center">
                    <div v-if="item.image" class="flex-shrink-0 h-10 w-10">
                      <img
                        class="h-10 w-10 rounded-full mr-4 object-cover"
                        :src="item.image"
                        :alt="item.name"
                      />
                    </div>
                    <div :class="{ 'ml-4 font-semibold': item.image }">
                      {{ item.text }}
                    </div>
                  </div>
                </td>
                <td
                  v-if="updates"
                  class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium"
                >
                  <div class="flex space-x-5 items-center text-gray-400">
                    <button
                      class="hover:text-black focus:outline-none"
                      @click="editItem(tbody[0].id)"
                    >
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
                          d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L16.732 3.732z"
                        />
                      </svg>
                    </button>
                    <button
                      class="hover:text-black focus:outline-none"
                      @click="deleteItem(tbody[0].id)"
                    >
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
                          d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"
                        />
                      </svg>
                    </button>
                  </div>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    thead: {
      type: Array,
      required: true,
    },
    data: {
      type: Array,
      required: true,
    },
    updates: Boolean,
  },
  data() {
    return {}
  },
  methods: {
    deleteItem(item) {
      this.$emit('delete', item)
    },
    editItem(item) {
      this.$emit('edit', item)
    },
  },
}
</script>
