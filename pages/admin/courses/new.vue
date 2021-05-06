<template>
  <div>
    <div class="mb-10 flex items-center justify-between">
      <div>
        <h1 class="text-2xl font-bold">Add new course</h1>
        <p class="text-gray-500">Fill the form</p>
      </div>
    </div>

    <form class="max-w-2xl">
      <div class="grid grid-cols-1 md:grid-cols-2 md:gap-x-10 md:gap-y-5">
        <Input placeholder="Name of course" name="name" type="text" />
        <Input placeholder="Max time" name="maxTime" type="text" />
        <Input placeholder="For what date" name="fromDate" type="text" />
        <Input placeholder="To what date" name="toDate" type="text" />
      </div>
      <div>
        <div class="flex justify-end items-center gap-6 mt-16">
          <nuxt-link
            to="/admin/courses/"
            class="text-gray-500 hover:text-gray-900"
            >Cancel</nuxt-link
          >
          <button
            name="submit"
            type="submit"
            class="px-10 py-4 bg-pink-500 hover:bg-pink-800 text-white font-semibold rounded"
          >
            Create new courses
          </button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  layout: 'admin',
  data() {
    return {
      options: ['Admin', 'Employee', 'Basic'],
    }
  },
}
</script>

<style></style>
