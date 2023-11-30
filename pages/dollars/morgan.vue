<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <ol class="flex gap-2 text-sm items-center">
        <li><NuxtLink to="/">Federal Issues</NuxtLink></li>
        <li><ChevronRightIcon class="w-4 h-4" /></li>
        <li>Dollars</li>
      </ol>
      <h1 class="text-3xl font-bold tracking-tight">Morgan Dollars</h1>
      <p>1878-1904, 1921</p>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 space-y-4">
    <Card>
      <template #header>Morgan Dollar</template>
      <template #subheader>1880-1904, 1921</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-40 h-40"
              src="/img/morgan-1898s.webp"
              placeholder
              loading="lazy"
            />
            <NuxtImg
              class="rounded-full w-40 h-40"
              src="/img/morgan-reverse.webp"
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
  { issue: "1921", VF: true },
  { issue: "1921-D" },
  { issue: "1921-S", VF: true },
  { issue: "1904" },
  { issue: "1904, Proof" },
  { issue: "1904-O" },
  { issue: "1904-S" },
  { issue: "1903" },
  { issue: "1903, Proof" },
  { issue: "1903-O" },
  { issue: "1903-S" },
  { issue: "1902" },
  { issue: "1902, Proof" },
  { issue: "1902-O" },
  { issue: "1902-S" },
  { issue: "1901" },
  { issue: "1901, Proof" },
  { issue: "1901-O" },
  { issue: "1901-S" },
  { issue: "1900" },
  { issue: "1900, Proof" },
  { issue: "1900-O" },
  { issue: "1900-S" },
  { issue: "1899" },
  { issue: "1899, Proof" },
  { issue: "1899-O" },
  { issue: "1899-S" },
  { issue: "1898", VF: true },
  { issue: "1898, Proof" },
  { issue: "1898-O" },
  { issue: "1898-S" },
  { issue: "1897" },
  { issue: "1897, Proof" },
  { issue: "1897-O" },
  { issue: "1897-S" },
  { issue: "1896", VF: true },
  { issue: "1896, Proof" },
  { issue: "1896-O" },
  { issue: "1896-S" },
  { issue: "1895" },
  { issue: "1895, Proof" },
  { issue: "1895-O" },
  { issue: "1895-S" },
  { issue: "1894" },
  { issue: "1894, Proof" },
  { issue: "1894-O" },
  { issue: "1894-S" },
  { issue: "1893" },
  { issue: "1893, Proof" },
  { issue: "1893-CC" },
  { issue: "1893-O" },
  { issue: "1893-S" },
  { issue: "1892" },
  { issue: "1892, Proof" },
  { issue: "1892-CC" },
  { issue: "1892-O" },
  { issue: "1892-S" },
  { issue: "1891" },
  { issue: "1891, Proof" },
  { issue: "1891-CC" },
  { issue: "1891-O" },
  { issue: "1891-S" },
  { issue: "1890" },
  { issue: "1890, Proof" },
  { issue: "1890-CC" },
  { issue: "1890-O" },
  { issue: "1890-S" },
  { issue: "1889" },
  { issue: "1889, Proof" },
  { issue: "1889-CC" },
  { issue: "1889-O" },
  { issue: "1889-S" },
  { issue: "1888" },
  { issue: "1888, Proof" },
  { issue: "1888-O" },
  { issue: "1888-S" },
  { issue: "1887" },
  { issue: "1887, Proof" },
  { issue: "1887-O" },
  { issue: "1887-S" },
  { issue: "1886" },
  { issue: "1886, Proof" },
  { issue: "1886-O" },
  { issue: "1886-S" },
  { issue: "1885" },
  { issue: "1885, Proof" },
  { issue: "1885-CC" },
  { issue: "1885-O" },
  { issue: "1885-S" },
  { issue: "1884" },
  { issue: "1884, Proof" },
  { issue: "1884-CC" },
  { issue: "1884-O", VF: true },
  { issue: "1884-S" },
  { issue: "1883" },
  { issue: "1883, Proof" },
  { issue: "1883-CC" },
  { issue: "1883-O" },
  { issue: "1883-S" },
  { issue: "1882" },
  { issue: "1882, Proof" },
  { issue: "1882-CC" },
  { issue: "1882-O" },
  { issue: "1882-S" },
  { issue: "1881" },
  { issue: "1881, Proof" },
  { issue: "1881-CC" },
  { issue: "1881-O" },
  { issue: "1881-S" },
  { issue: "1880" },
  { issue: "1880, Proof" },
  { issue: "1880-CC" },
  { issue: "1880-O" },
  { issue: "1880-S" },
  { issue: "1879" },
  { issue: "1879, Proof" },
  { issue: "1879-CC" },
  { issue: "1879-O" },
  { issue: "1879-S" },
  { issue: "1878" },
  { issue: "1878, Proof" },
  { issue: "1878-CC" },
  { issue: "1878-S" },
];
</script>
