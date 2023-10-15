<template>
  <p>Lincoln, Shield Reverse</p>
  <div
    class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4"
  >
    <div
      v-for="x in 10"
      class="relative flex flex-col rounded shadow-md divide-y h-fit"
    >
      <div class="py-2 px-4">
        <span class="font-semibold">{{ 2024 - x }}</span>
      </div>
      <ul class="flex flex-col divide-y h-fit">
        <li
          v-for="strike in ['Avg', 'Unc', 'Pf']"
          class="flex justify-between py-2 px-4"
        >
          {{ strike }}
          <ul class="text-center flex gap-1">
            <li
              v-if="strike != 'Pf'"
              class="border shadow rounded px-2 w-7 h-7"
            >
              <span class="text-sm">P</span>
            </li>
            <li
              v-if="strike != 'Pf'"
              class="border shadow rounded px-2 w-7 h-7"
            >
              <span class="text-sm">D</span>
            </li>
            <li
              v-if="x == 5 && strike == 'Unc'"
              class="border shadow rounded px-2 w-7 h-7"
            >
              <span class="text-sm">W</span>
            </li>
            <li
              v-if="strike == 'Pf'"
              class="border shadow rounded px-2 w-7 h-7"
            >
              <span class="text-sm">S</span>
            </li>
            <li
              v-if="x == 5 && strike == 'Pf'"
              class="border shadow rounded px-2 w-7 h-7"
            >
              <span class="text-sm">W</span>
            </li>
          </ul>
        </li>
        <li v-if="x == 5" class="flex justify-between py-2 px-4">
          RevPf
          <ul class="text-center flex gap-1">
            <li class="border shadow rounded px-2 w-7 h-7">
              <span class="text-sm">W</span>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const strikes = ["Avg", "Unc", "Pf"];
</script>
