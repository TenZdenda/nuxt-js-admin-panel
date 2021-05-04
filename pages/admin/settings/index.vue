<template>
  <div class="space-y-16">
    <div>
      <h1 class="text-2xl font-bold">Settings page</h1>
      <p class="text-gray-500">Edit your page</p>
    </div>

    <form class="max-w-2xl space-y-10">
      <section class="space-y-5">
        <h2 class="text-xl font-bold">General Settings</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 md:gap-x-10 md:gap-y-5">
          <Input placeholder="Name of page" name="name" type="text" />
          <Input placeholder="Email address" name="email" type="email" />
          <Input placeholder="Phone number" name="phone" type="phone" />
        </div>
      </section>

      <section class="space-y-5">
        <h2 class="text-xl font-bold">Social media</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 md:gap-x-10 md:gap-y-5">
          <Input
            placeholder="Facebook page (url)"
            name="facebook"
            type="text"
          />
          <Input placeholder="Twitter page (url)" name="twitter" type="text" />
          <Input
            placeholder="Instagram page (url)"
            name="instagram"
            type="text"
          />
        </div>
      </section>

      <div>
        <div class="flex justify-end items-center gap-6 mt-16">
          <button
            name="submit"
            type="submit"
            class="px-10 py-4 bg-pink-500 hover:bg-pink-800 text-white font-semibold rounded"
          >
            Save settings
          </button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  layout: 'admin',
}
</script>
