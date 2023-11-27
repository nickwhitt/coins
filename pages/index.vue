<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <h1 class="text-3xl font-bold tracking-tight">Federal Issues</h1>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 lg:columns-2 space-y-4">
    <article
      v-for="series in coins"
      class="border sm:rounded-lg break-inside-avoid-column bg-white"
    >
      <h2 class="text-lg font-bold px-6 py-2 border-b">
        {{ series.denomination }}
      </h2>
      <ol class="grid sm:grid-cols-2 gap-2 px-4 py-2">
        <li v-for="coin in series.types">
          <figure class="flex items-center">
            <NuxtLink :to="coin.slug" class="contents">
              <NuxtImg
                v-if="coin.obv"
                :src="coin.obv"
                placeholder
                loading="lazy"
                width="80px"
                height="80px"
              />
              <img v-else class="rounded-full w-20 h-20 bg-slate-300" />
              <figcaption class="ml-2">
                <p class="text-lg">
                  {{ coin.type }}
                </p>
                <p>{{ coin.dates }}</p>
              </figcaption>
            </NuxtLink>
          </figure>
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
      {
        type: "Lincoln",
        dates: "since 1909",
        slug: "/cents",
        obv: "/img/lincoln-2023.webp",
      },
    ],
  },
  {
    denomination: "Two and Three Cents",
    types: [
      { type: "Two Cent", dates: "1864-1873" },
      { type: "Three Cent Silver", dates: "1851-1873" },
      { type: "Three Cent Nickel", dates: "1865-1889" },
    ],
  },
  {
    denomination: "Nickel Five Cents",
    types: [
      {
        type: "Shield",
        dates: "1866-1883",
        obv: "/img/nickel-shield-1883.webp",
      },
      {
        type: "Liberty",
        dates: "1883-1913",
        obv: "/img/nickel-liberty-1883.webp",
      },
      {
        type: "Buffalo",
        dates: "1913-1938",
        obv: "/img/nickel-buffalo-1913.webp",
      },
      {
        type: "Jefferson",
        dates: "since 1938",
        obv: "/img/jefferson-2023p.webp",
      },
    ],
  },
  {
    denomination: "Half Dimes",
    types: [
      { type: "Bust", dates: "1792" },
      { type: "Flowing Hair", dates: "1794-1795" },
      { type: "Draped Bust", dates: "1796-1805" },
      { type: "Capped Bust", dates: "1829-1837" },
      { type: "Liberty Seated", dates: "1837-1873" },
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
      {
        type: "Roosevelt",
        dates: "since 1946",
        obv: "/img/roosevelt-2023p.webp",
      },
    ],
  },
  {
    denomination: "Twenty Cents",
    types: [{ type: "Twenty Cent", dates: "1875-1878" }],
  },
  {
    denomination: "Quarter Dollars",
    types: [
      { type: "Draped Bust", dates: "1796-1807" },
      { type: "Capped Bust", dates: "1815-1838" },
      { type: "Liberty Seated", dates: "1838-1891" },
      { type: "Barber", dates: "1892-1916" },
      { type: "Standing Liberty", dates: "1916-1930" },
      {
        type: "Washington",
        dates: "since 1932",
        obv: "/img/washington-2021p.webp",
      },
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
      {
        type: "Kennedy",
        dates: "since 1964",
        obv: "/img/kennedy-2023p.webp",
      },
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
      {
        type: "Sacagawea",
        dates: "since 2000",
        obv: "/img/sacagawea-2000p.webp",
      },
      {
        type: "Presidential",
        dates: "2007-2016, 2020",
        obv: "/img/presidential-dollar-reverse.webp",
      },
      {
        type: "Innovation",
        dates: "2018-2032",
        obv: "/img/innovation-dollar-obverse.webp",
      },
    ],
  },
  {
    denomination: "Gold Dollars",
    types: [
      { type: "One Dollar", dates: "1849-1889" },
      { type: "Three Dollar", dates: "1854-1889" },
      { type: "Stella", dates: "1879-1880" },
    ],
  },
  {
    denomination: "Quarter Eagles",
    types: [
      { type: "Draped Bust", dates: "1796-1807" },
      { type: "Capped Bust", dates: "1808-1834" },
      { type: "Classic Head", dates: "1834-1839" },
      { type: "Liberty Head", dates: "1840-1907" },
      { type: "Indian", dates: "1908-1929" },
    ],
  },
  {
    denomination: "Half Eagles",
    types: [
      { type: "Draped Bust", dates: "1795-1807" },
      { type: "Capped Bust", dates: "1807-1834" },
      { type: "Classic Head", dates: "1834-1838" },
      { type: "Liberty Head", dates: "1839-1908" },
      { type: "Indian", dates: "1908-1929" },
    ],
  },
  {
    denomination: "Eagles",
    types: [
      { type: "Draped Bust", dates: "1795-1804" },
      { type: "Liberty Head", dates: "1838-1907" },
      { type: "Indian", dates: "1907-1933" },
    ],
  },
  {
    denomination: "Double Eagles",
    types: [
      { type: "Liberty Head", dates: "1849-1907" },
      { type: "St. Gaudens", dates: "1907-1933" },
    ],
  },
];
</script>
