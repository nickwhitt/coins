<template>
  <ul class="divide-y leading-loose">
    <li>
      <ul class="flex justify-between items-center">
        <li class="font-bold">Issue</li>
        <li>
          <ul class="flex font-bold text-center">
            <li v-for="grade in grades" class="capitalize w-10">
              {{ grade }}
            </li>
          </ul>
        </li>
      </ul>
    </li>
    <li v-for="row in rows">
      <ul class="flex justify-between items-center">
        <li>{{ row.issue }}</li>
        <li>
          <ul class="flex">
            <li v-for="grade in grades" class="w-10">
              <img
                v-if="row[grade]"
                class="rounded-full w-4 h-4 bg-green-500 mx-auto"
              />
            </li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</template>

<script setup>
const props = defineProps(["rows"]);
const grades = ["cir", "unc", "pf"];
</script>
