<template>
  <Body class="bg-gray-50" />
  <header class="bg-gray-800 text-gray-400 h-12 flex items-center">
    <nav class="container mx-auto px-2 flex items-center justify-between">
      <NuxtLink to="/" class="text-gray-200 text-xl">Coins</NuxtLink>
      <ul class="hidden sm:flex">
        <li v-for="link in links" class="pl-4">
          <NuxtLink :to="link.slug ?? '#'" class="hover:text-gray-200">
            {{ link.denomination }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </header>

  <div class="container mx-auto px-2">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>

    <footer class="border-t mt-8">
      <nav class="text-sm py-2 hidden sm:flex sm:justify-center gap-4">
        <figure v-for="link in links">
          <figcaption class="font-bold uppercase">
            {{ link.denomination }}
          </figcaption>
          <ul>
            <li v-for="type in link.types" class="hover:underline">
              <NuxtLink to="#">{{ type.title }}</NuxtLink>
            </li>
          </ul>
        </figure>
      </nav>
    </footer>
  </div>
</template>

<script setup>
const links = [
  {
    denomination: "Cents",
    types: [
      { title: "Lincoln" },
      { title: "Indian Head" },
      { title: "Flying Eagle" },
    ],
  },
  {
    denomination: "Nickels",
    types: [
      { title: "Jefferson" },
      { title: "Buffalo" },
      { title: "Liberty Head" },
      { title: "Shield" },
    ],
  },
  {
    denomination: "Dimes",
    types: [
      { title: "Roosevelt" },
      { title: "Mercury" },
      { title: "Barber" },
      { title: "Liberty Seated" },
      { title: "Capped Bust" },
      { title: "Draped Bust" },
    ],
  },
  {
    denomination: "Quarters",
    slug: "quarters",
    types: [
      { title: "American Women" },
      { title: "America the Beautiful" },
      { title: "States and Territories" },
      { title: "Washington" },
      { title: "Standing Liberty" },
      { title: "Barber" },
      { title: "Liberty Seated" },
      { title: "Capped Bust" },
      { title: "Draped Bust" },
    ],
  },
  {
    denomination: "Half Dollars",
    types: [
      { title: "Kennedy" },
      { title: "Franklin" },
      { title: "Liberty Walking" },
      { title: "Barber" },
      { title: "Liberty Seated" },
      { title: "Capped Bust" },
      { title: "Draped Bust" },
      { title: "Flowing Hair" },
    ],
  },
];
</script>
