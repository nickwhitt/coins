<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <ol class="flex gap-2 text-sm items-center">
        <li><NuxtLink to="/">Federal Issues</NuxtLink></li>
        <li><ChevronRightIcon class="w-4 h-4" /></li>
        <li>Dollars</li>
      </ol>
      <h1 class="text-3xl font-bold tracking-tight">Peace Dollars</h1>
      <p>1921-1935</p>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 space-y-4">
    <Card>
      <template #header>Peace Dollar</template>
      <template #subheader>1921-1935</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-40 h-40"
              src="/img/peace-1923d.webp"
              placeholder
              loading="lazy"
            />
            <NuxtImg
              class="rounded-full w-40 h-40"
              src="/img/peace-d-reverse.webp"
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
const coins = [
  { issue: "1935" },
  { issue: "1935-S" },
  { issue: "1934" },
  { issue: "1934-D" },
  { issue: "1934-S" },
  { issue: "1928" },
  { issue: "1928-S" },
  { issue: "1927" },
  { issue: "1927-D" },
  { issue: "1927-S" },
  { issue: "1926" },
  { issue: "1926-D" },
  { issue: "1926-S" },
  { issue: "1925" },
  { issue: "1925-S" },
  { issue: "1924" },
  { issue: "1924-S" },
  { issue: "1923" },
  { issue: "1923-D" },
  { issue: "1923-S" },
  { issue: "1922" },
  { issue: "1922, Proof, High Relief" },
  { issue: "1922-D" },
  { issue: "1922-S" },
  { issue: "1921" },
];
</script>
