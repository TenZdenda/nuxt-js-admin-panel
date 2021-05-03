<template>
  <div>
    <div class="mb-10 flex items-center">
      <div class="bg-pink-100 rounded-full py-2 px-3 text-2xl">🤠</div>
      <div class="ml-5">
        <h1 class="text-2xl font-bold">Hello Zdeněk Pašek 👋🏼</h1>
        <p class="text-gray-500">How are you today?</p>
      </div>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 gap-5">
      <StatsCard
        name="Your monthly income 💰"
        record="1,283.93 $"
        :dup="true"
        :dpercent="56"
      />

      <StatsCard
        name="Your monthly income 💰"
        record="20 x"
        :dup="false"
        :dpercent="96"
      />

      <StatsCard
        name="Your monthly income 💰"
        record="18,343.93 $"
        :dup="true"
        :dpercent="203"
      />
    </div>
  </div>
</template>

<script>
export default {
  layout: 'admin',
}
</script>
