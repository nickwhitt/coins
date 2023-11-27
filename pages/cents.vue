<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";
import { CheckCircleIcon } from "@heroicons/vue/20/solid";
const { data: types } = await useFetch("/api/cents/lincoln");
</script>

<template>
  <Body class="bg-gray-100" />
  <main class="md:container mx-auto sm:px-4">
    <hgroup class="py-8 px-4 sm:px-o">
      <ol class="flex gap-2 text-sm items-center">
        <li>Federal Issues</li>
        <li><ChevronRightIcon class="w-4 h-4" /></li>
        <li>Small Cents</li>
      </ol>
      <h1 class="text-3xl font-bold tracking-tight">Lincoln Obverse</h1>
    </hgroup>
    <article v-for="type in types" class="shadow mb-6 bg-white">
      <hgroup class="px-6 py-5 border-b">
        <h2 class="text-lg font-bold">{{ type.type }}</h2>
        <p>{{ type.dates }}</p>
      </hgroup>
      <div
        class="grid grid-cols-3 sm:grid-cols-4 lg:grid-cols-6 gap-4 px-6 py-5"
      >
        <figure v-for="issue in type.issues" class="flex flex-col items-center">
          <div class="inline-block relative">
            <NuxtImg
              :src="issue.rev || type.rev"
              placeholder
              loading="lazy"
              width="80px"
              height="80px"
            />
            <CheckCircleIcon
              v-if="issue.have"
              class="fill-emerald-700 absolute bottom-0 right-0 h-8 w-8"
            />
          </div>
          <figcaption class="text-center">
            <p>{{ issue.issue }}</p>
            <p class="font-light text-sm">{{ issue.variant }}</p>
          </figcaption>
        </figure>
      </div>
    </article>
  </main>
</template>
