<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <!-- <ol class="flex gap-2 text-sm items-center">
        <li>Federal Issues</li>
        <li><ChevronRightIcon class="w-4 h-4" /></li>
        <li>Small Cents</li>
      </ol> -->
      <h1 class="text-3xl font-bold tracking-tight">Federal Issues</h1>
    </hgroup>
  </div>

  <main class="container mx-auto px-4 md:columns-2 space-y-4">
    <article
      v-for="denom in coins"
      class="border rounded-lg border-slate-400 break-inside-avoid-column bg-white"
    >
      <h2 class="text-lg font-bold p-2 border-b border-slate-400">
        {{ denom.denomination }}
      </h2>
      <ol class="sm:columns-2 md:columns-1 lg:columns-2 p-2">
        <li v-for="coin in denom.types" class="flex items-center py-1">
          <NuxtLink :to="coin.slug" class="contents">
            <img class="rounded-full w-16 h-16 bg-slate-300" />
            <img
              class="hidden sm:flex lg:hidden xl:flex rounded-full w-16 h-16 bg-slate-300 ml-0.5"
            />
            <div class="ml-2">
              <p class="text-lg">
                {{ coin.type }}
              </p>
              <p>{{ coin.dates }}</p>
            </div>
          </NuxtLink>
        </li>
      </ol>
    </article>
  </main>

  <footer class="p-4"></footer>
</template>

<script setup>
const coins = [
  {
    denomination: "Half Cents",
    types: [
      { type: "Liberty Cap", dates: "1793-1797" },
      { type: "Draped Bust", dates: "1800-1808" },
      { type: "Classic Head", dates: "1809-1836" },
      { type: "Braided Hair", dates: "1840-1857" },
    ],
  },
  {
    denomination: "Cents",
    types: [
      { type: "Draped Bust", dates: "1796-1807" },
      { type: "Classic Head", dates: "1808-1814" },
      { type: "Coronet Head", dates: "1816-1839" },
      { type: "Braided Hair", dates: "1839-1857" },
      { type: "Flying Eagle", dates: "1856-1858" },
      { type: "Indian", dates: "1859-1909" },
      { type: "Lincoln", dates: "since 1909", slug: "/cents" },
    ],
  },
  {
    denomination: "Nickels",
    types: [
      { type: "Shield", dates: "1866-1883" },
      { type: "Liberty", dates: "1883-1913" },
      { type: "Buffalo", dates: "1913-1938" },
      { type: "Jefferson", dates: "since 1938" },
    ],
  },
  {
    denomination: "Dimes",
    types: [
      { type: "Draped Bust", dates: "1796-1807" },
      { type: "Capped Bust", dates: "1809-1837" },
      { type: "Liberty Seated", dates: "1837-1891" },
      { type: "Barber", dates: "1892-1916" },
      { type: "Mercury", dates: "1916-1945" },
      { type: "Roosevelt", dates: "since 1946" },
    ],
  },
  {
    denomination: "Quarters",
    types: [
      { type: "Draped Bust", dates: "1796-1807" },
      { type: "Capped Bust", dates: "1815-1838" },
      { type: "Liberty Seated", dates: "1838-1891" },
      { type: "Barber", dates: "1892-1916" },
      { type: "Standing Liberty", dates: "1916-1930" },
      { type: "Washington", dates: "since 1932" },
    ],
  },
  {
    denomination: "Half Dollars",
    types: [
      { type: "Flowing Hair", dates: "1794-1795" },
      { type: "Draped Bust", dates: "1796-1807" },
      { type: "Capped Bust", dates: "1807-1839" },
      { type: "Liberty Seated", dates: "1839-1891" },
      { type: "Barber", dates: "1892-1915" },
      { type: "Walking Liberty", dates: "1916-1947" },
      { type: "Franklin", dates: "1948-1963" },
      { type: "Kennedy", dates: "since 1964" },
    ],
  },
  {
    denomination: "Dollars",
    types: [
      { type: "Flowing Hair", dates: "1794-1795" },
      { type: "Draped Bust", dates: "1795-1804" },
      { type: "Liberty Seated", dates: "1836-1873" },
      { type: "Trade", dates: "1873-1885" },
      { type: "Morgan", dates: "1878-1921" },
      { type: "Peace", dates: "1921-1935" },
      { type: "Eisenhower", dates: "1971-1978" },
      { type: "Susan B. Anthony", dates: "1979-1999" },
      { type: "Sacagawea", dates: "since 2000" },
      { type: "Presidential", dates: "2007-2016, 2020" },
      { type: "Innovation", dates: "2018-2032" },
    ],
  },
];
</script>
