<template>
  <Body class="bg-slate-50" />
  <header class="bg-slate-800 text-slate-400">
    <Disclosure as="nav" class="container mx-auto px-2" v-slot="{ open }">
      <div class="relative flex items-center h-16">
        <div class="absolute flex inset-y-0 left-0 sm:hidden">
          <DisclosureButton class="relative">
            <span class="absolute -inset-0.5" />
            <span class="sr-only">Open main menu</span>
            <Bars3Icon v-if="!open" class="block h-6 w-6" aria-hidden="true" />
            <XMarkIcon v-else class="block h-6 w-6" aria-hidden="true" />
          </DisclosureButton>
        </div>

        <div class="flex flex-1 items-center justify-center sm:justify-between">
          <NuxtLink to="/" class="text-slate-200 text-xl">Coins</NuxtLink>
          <div class="hidden sm:block">
            <div class="flex space-x-4 ml-6">
              <NuxtLink
                v-for="link in links"
                :to="link.slug ?? '#'"
                class="hover:text-slate-200"
              >
                {{ link.denomination }}
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>

      <DisclosurePanel class="sm:hidden">
        <NuxtLink
          v-for="link in links"
          :to="link.slug ?? '#'"
          class="block hover:text-slate-200 p-2"
        >
          {{ link.denomination }}
        </NuxtLink>
      </DisclosurePanel>
    </Disclosure>
  </header>

  <div class="container mx-auto px-2">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>

  <footer class="bg-slate-200 mt-8">
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
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";

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
