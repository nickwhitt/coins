<script setup>
const { data: cent } = await useFetch("/api/cents/lincoln");
</script>

<template>
  <div>
    <div v-for="type in cent.types">
      <h2>{{ type.type }}</h2>
      <div
        class="grid grid-cols-3 sm:grid-cols-4 md:grid-cols-5 lg:grid-cols-6 gap-4"
      >
        <figure v-for="issue in type.issues">
          <img class="rounded-full w-[1.9cm] h-[1.9cm] bg-slate-300 mx-auto" />
          <figcaption class="text-center">
            <p>{{ issue.issue }}</p>
            <p class="font-light text-sm">{{ issue.variant }}</p>
          </figcaption>
        </figure>
      </div>
    </div>
  </div>
</template>
