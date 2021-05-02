<template>
  <div>
    <div class="mb-10">
      <h1 class="text-2xl font-bold">Hello Zdeněk Pašek 👋🏼</h1>
      <p class="text-gray-500">How are you today?</p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 gap-5">
      <div class="w-full h-auto border border-gray-100 rounded">
        <div class="p-10">
          <h2 class="text-gray-600 text-xl">Your monthly income 💰</h2>
          <p class="text-4xl font-bold my-4">1,239.48 $</p>
          <div class="flex items-center">
            <div class="p-1 rounded-full bg-green-100 text-green-500">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-4 w-4"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"
                />
              </svg>
            </div>
            <p class="ml-2 text-gray-400">
              <span class="text-green-500 font-bold">+ 50 %</span> vs last month
            </p>
          </div>
        </div>
      </div>
      <div class="w-full h-auto border border-gray-100 rounded">
        <div class="p-10">
          <h2 class="text-gray-600 text-xl">Lorem ipsum 👀</h2>
          <p class="text-4xl font-bold my-4">14 x</p>
          <div class="flex items-center">
            <div class="p-1 rounded-full bg-red-100 text-red-500">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-4 w-4"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M13 17h8m0 0V9m0 8l-8-8-4 4-6-6"
                />
              </svg>
            </div>
            <p class="ml-2 text-gray-400">
              <span class="text-red-500 font-bold">- 13 %</span> vs last month
            </p>
          </div>
        </div>
      </div>
      <div class="w-full h-auto border border-gray-100 rounded">
        <div class="p-10">
          <h2 class="text-gray-600 text-xl">Lorem ipsum 👽</h2>
          <p class="text-4xl font-bold my-4">20,048.87 $</p>
          <div class="flex items-center">
            <div class="p-1 rounded-full bg-green-100">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-4 w-4 text-green-500"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"
                />
              </svg>
            </div>
            <p class="ml-2 text-gray-400">
              <span class="text-green-500 font-bold">+ 138 %</span> vs last
              month
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'admin',
}
</script>
