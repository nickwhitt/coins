<template>
  <p class="text-2xl my-8">ATB 2019</p>
  <div
    class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4"
  >
    <div
      v-for="issue in atb2019"
      class="flex flex-col rounded shadow-md divide-y h-fit bg-white"
    >
      <div class="py-2 px-4 bg-slate-200">
        <span class="font-semibold">{{ issue.reverse }}</span>
        <span class="text-sm font-light pl-1">{{ issue.state }}</span>
      </div>
      <ul class="flex flex-col divide-y h-fit">
        <li
          v-for="issue in issue.issues"
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
const { data: atb2019 } = await useFetch("/api/atb");
</script>
