<template>
  <div>
    <div class="mb-10 flex items-center justify-between">
      <div>
        <h1 class="text-2xl font-bold">Add new user</h1>
        <p class="text-gray-500">Fill the form</p>
      </div>
    </div>

    <form class="max-w-2xl">
      <div class="grid grid-cols-1 md:grid-cols-2 md:gap-x-10 md:gap-y-5">
        <Input placeholder="First name" name="firstname" type="text" />
        <Input placeholder="Last name" name="lastname" type="text" />
        <Input placeholder="E-mail address" name="email" type="email" />
        <SelectInput id="role" name="role" :options="options" />
      </div>
      <div>
        <div class="flex justify-end items-center gap-6 mt-16">
          <nuxt-link to="/admin/users" class="text-gray-500 hover:text-gray-900"
            >Cancel</nuxt-link
          >
          <button
            name="submit"
            type="submit"
            class="
              px-10
              py-4
              bg-pink-500
              hover:bg-pink-800
              text-white
              font-semibold
              rounded
            "
          >
            Create new user
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
