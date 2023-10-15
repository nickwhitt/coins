<template>
  <p>Lincoln, Shield Reverse</p>
  <div
    class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4"
  >
    <div
      v-for="shield in data"
      class="flex flex-col rounded shadow-md divide-y h-fit bg-white"
    >
      <div class="py-2 px-4 bg-slate-200">
        <span class="font-semibold">{{ shield.date }}</span>
      </div>
      <ul class="flex flex-col divide-y h-fit">
        <li
          v-for="issue in shield.issues"
          class="flex justify-between py-2 px-4"
        >
          {{ issue.strike }}
          <ul class="text-center flex gap-1">
            <li
              v-for="mint in issue.mints"
              class="border shadow rounded px-2 w-7 h-7"
              :class="{ 'bg-emerald-400': mint.have }"
            >
              <span class="text-sm">{{ mint.mark }}</span>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const { data } = await useFetch("/api/cents/lincoln/shield");
</script>
