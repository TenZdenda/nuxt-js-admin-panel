<template>
  <div class="h-screen flex">
    <!-- Fixed sidebar -->
    <Sidebar />
    <!-- Scroll wrapper -->
    <div class="flex-1 flex overflow-hidden">
      <!-- Scrollable container -->
      <div class="flex-1 overflow-y-scroll">
        <div class="flex items-center justify-end px-6 py-4">
          <nuxt-link
            to="/profile"
            class="flex items-center p-2 hover:bg-gray-100 rounded-full"
          >
            <img
              class="h-10 w-10 md:h-12 md:w-12 rounded-full"
              src="https://zdenekpasek.com/images/me.jpg"
              alt="Zdeněk"
            />
            <div class="ml-4 hidden md:block">
              <p class="font-bold">Zdeněk Pašek</p>
              <p class="text-gray-500">hello@zdenekpasek.com</p>
            </div>
          </nuxt-link>
        </div>
        <div class="p-6">
          <Nuxt />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>
