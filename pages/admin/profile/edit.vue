<template>
  <div class="space-y-16">
    <div class="flex justify-between items-center">
      <div>
        <h1 class="text-2xl font-bold">Edit your profile</h1>
        <p class="text-gray-500">Edit, edit, edit</p>
      </div>
      <nuxt-link
        to="/admin/profile"
        class="
          bg-gray-100
          hover:bg-gray-300
          text-gray-400
          hover:text-gray-600
          font-semibold
          py-2
          px-6
          rounded
          mx-auto
          md:mx-0
          my-4
          md:my-0
          block
          focus:outline-none
        "
        >Back to profile</nuxt-link
      >
    </div>

    <div class="max-w-2xl space-y-10">
      <form>
        <section class="space-y-5">
          <h2 class="text-xl font-bold">General Settings</h2>
          <div class="grid grid-cols-1 md:grid-cols-2 md:gap-x-10 md:gap-y-5">
            <Input placeholder="Your first name" name="firstname" type="text" />
            <Input placeholder="Your last name" name="lastname" type="text" />
            <Input placeholder="Your email" name="email" type="email" />
          </div>
        </section>

        <div class="flex justify-end items-center gap-6 mt-16">
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
            Save
          </button>
        </div>
      </form>

      <hr />

      <form>
        <section class="space-y-5">
          <h2 class="text-xl font-bold">Password</h2>
          <div class="md:space-y-5">
            <Input
              placeholder="Your old password"
              name="oldPassword"
              type="password"
            />

            <div class="md:flex md:space-x-10">
              <Input
                placeholder="Your new password"
                name="newPassword"
                type="password"
              />
              <Input
                placeholder="Your new password again"
                name="newPasswordAgain"
                type="password"
              />
            </div>
          </div>
        </section>
        <div class="flex justify-end items-center gap-6 mt-16">
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
            Save
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'admin',
}
</script>
