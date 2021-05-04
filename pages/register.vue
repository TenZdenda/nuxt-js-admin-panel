<template>
  <div class="px-10 md:px-0 w-full md:w-96">
    <div class="mb-12">
      <h1 class="text-3xl font-bold">Hello stranger 🙌</h1>
      <span class="text-xl block text-gray-500">Don’t be shy and join us!</span>
    </div>
    <form>
      <Input placeholder="Your first name" type="text" name="firstname" />

      <Input placeholder="Your last name" type="text" name="lastname" />

      <Input placeholder="Your e-mail address" type="email" name="email" />

      <Input placeholder="Your password" type="password" name="password" />

      <button
        type="submit"
        class="bg-pink-500 text-white py-3 px-14 font-bold mx-auto block rounded mt-10"
      >
        Sign up
      </button>

      <hr class="my-10" />

      <p class="text-center block mt-5 text-black">
        Already have an account?
        <nuxt-link to="/login" class="font-bold hover:text-pink-700"
          >Sign in</nuxt-link
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
