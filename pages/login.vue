<template>
  <div class="px-10 md:px-0 w-full md:w-96">
    <div class="mb-12">
      <h1 class="text-3xl font-bold">Hello 👋,</h1>
      <span class="text-xl block text-gray-500">Sign in and do something</span>
    </div>
    <form>
      <Input placeholder="Your e-mail address" type="email" name="email" />

      <Input placeholder="Your password" type="password" name="password" />

      <button
        type="submit"
        class="bg-pink-500 text-white py-3 px-14 font-bold mx-auto block rounded mt-10"
      >
        Sign in
      </button>

      <hr class="my-10" />

      <p class="text-center block mt-5 text-black">
        Don't have an account?
        <nuxt-link to="/register" class="font-bold hover:text-pink-700"
          >Create one</nuxt-link
        >!
      </p>
    </form>
  </div>
</template>

<script>
export default {
  layout: 'auth',
}
</script>
