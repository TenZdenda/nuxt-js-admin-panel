<template>
  <div>
    <div class="md:flex md:justify-between md:items-center">
      <div class="flex gap-5 md:gap-10 items-center">
        <img
          src="https://zdenekpasek.com/images/me.jpg"
          alt="Zdeněk Pašek"
          class="h-20 w-20 md:h-24 md:w-24 rounded-xl"
        />
        <div>
          <p class="text-2xl md:text-3xl font-bold">Zdeněk Pašek</p>
          <p class="md:text-xl text-gray-400">hello@zdenekpasek.com</p>
        </div>
      </div>

      <nuxt-link
        to="/admin/profile/edit"
        class="bg-gray-100 hover:bg-gray-300 text-gray-400 hover:text-gray-600 font-semibold py-2 px-6 rounded mx-auto md:mx-0 my-4 md:my-0 block focus:outline-none"
      >
        Edit profile
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'admin',
}
</script>
