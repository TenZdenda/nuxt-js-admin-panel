<template>
  <select
    :id="id"
    :name="name"
    class="
      w-full
      block
      h-15
      py-4
      px-5
      my-2
      bg-gray-100
      rounded-md
      focus:outline-none
    "
  >
    <option value="" disabled selected>Select your option</option>
    <option v-for="option in options" :key="option">{{ option }}</option>
  </select>
</template>

<script>
export default {
  name: 'SelectInput',
  props: {
    name: {
      type: String,
      required: true,
    },
    id: {
      type: String,
      required: true,
    },
    options: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style></style>
