<template>
  <div class="container mx-auto p-2">
    <p>ATB 2019</p>
    <div
      class="grid sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 2xl:grid-cols-5 gap-4"
    >
      <div
        v-for="issue in atb2019"
        class="relative flex flex-col rounded shadow-md divide-y h-fit"
      >
        <div class="py-2 px-4">
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
  </div>
</template>

<script setup>
const { data: atb2019 } = await useFetch("/api/atb");
</script>
