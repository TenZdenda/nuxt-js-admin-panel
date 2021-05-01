<template>
  <div class="h-screen md:flex">
    <!-- Fixed sidebar -->
    <div class="hidden md:block bg-gray-600 w-4/12 h-screen rounded-r-2xl">
      <!-- Sidebar content -->
    </div>
    <!-- Scroll wrapper -->
    <div class="flex-1 flex overflow-hidden">
      <!-- Scrollable container -->
      <div class="flex-1 overflow-y-scroll">
        <div class="flex h-screen">
          <div class="m-auto">
            <Nuxt />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
