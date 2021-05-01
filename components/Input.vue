<template>
  <input
    :type="type"
    :placeholder="placeholder"
    :name="name"
    class="w-full h-15 px-5 py-4 my-2 outline-none rounded bg-gray-100"
  />
</template>

<script>
export default {
  name: 'Input',
  props: ['placeholder', 'type', 'name'],
}
</script>
