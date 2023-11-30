<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <ol class="flex gap-2 text-sm items-center">
        <li><NuxtLink to="/">Federal Issues</NuxtLink></li>
        <li><ChevronRightIcon class="w-4 h-4" /></li>
        <li>Dollars</li>
      </ol>
      <h1 class="text-3xl font-bold tracking-tight">Anthony Dollars</h1>
      <p>1921-</p>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 space-y-4">
    <Card>
      <template #header>Susan B. Anthony Dollar</template>
      <template #subheader>1979-</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/anthony-1979s.webp"
              placeholder
              loading="lazy"
            />
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/anthony-reverse.webp"
              placeholder
              loading="lazy"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Circulation strike
          </figcaption>
        </figure>
      </div>

      <div class="grid lg:grid-cols-2 gap-4">
        <CoinList :rows="coins" class="lg:hidden" />
        <CoinList
          :rows="coins.slice(0, Math.floor(coins.length / 2))"
          class="hidden lg:grid"
        />
        <CoinList
          :rows="coins.slice(Math.floor(coins.length / 2), coins.length)"
          class="hidden lg:grid"
        />
      </div>
    </Card>
  </main>

  <footer class="p-4"></footer>
</template>

<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";
const coins = [];
</script>
