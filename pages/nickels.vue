<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <h1 class="text-3xl font-bold tracking-tight">Jefferson Nickels</h1>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 lg:columns-2 space-y-4">
    <article class="border sm:rounded-lg break-inside-avoid-column bg-white">
      <hgroup class="px-6 py-2 flex justify-between items-baseline border-b">
        <h2 class="text-xl font-bold">Jefferson, Modified</h2>
        <ul class="flex flex-row font-bold text-center">
          <li v-for="grade in grades" class="w-8">
            {{ grade.toUpperCase() }}
          </li>
        </ul>
      </hgroup>
      <div class="px-6 divide-y leading-loose">
        <ul v-for="coin in coins" class="flex justify-between items-center">
          <li>{{ coin.issue }}</li>
          <li>
            <ul class="flex">
              <li v-for="grade in grades" class="w-8">
                <img
                  v-if="coin[grade]"
                  class="rounded-full w-4 h-4 bg-green-500 mx-auto"
                />
              </li>
            </ul>
          </li>
        </ul>
      </div>
    </article>
  </main>

  <footer class="p-4"></footer>
</template>

<script setup>
const grades = ["vg", "f", "vf", "ef", "au", "ms", "pf"];
const coins = [
  { issue: "2023-P", au: true },
  { issue: "2023-D" },
  { issue: "2023-S, Proof" },
  { issue: "2022-P", au: true },
  { issue: "2022-D" },
  { issue: "2022-S, Proof" },
  { issue: "2021-P", au: true },
  { issue: "2021-D", au: true },
  { issue: "2021-S, Proof" },
  { issue: "2020-P", au: true },
  { issue: "2020-D", au: true },
  { issue: "2020-S, Proof" },
  { issue: "2019-P", au: true },
  { issue: "2019-D", au: true },
  { issue: "2019-S, Proof" },
  { issue: "2018-P", au: true },
  { issue: "2018-D", vf: true },
  { issue: "2018-S, Proof" },
  { issue: "2017-P", ef: true },
  { issue: "2017-D", ef: true },
  { issue: "2017-S, Proof" },
  { issue: "2016-P", vf: true },
  { issue: "2016-D", vf: true },
  { issue: "2016-S, Proof" },
  { issue: "2015-P", f: true },
  { issue: "2015-D", f: true },
  { issue: "2015-S, Proof" },
  { issue: "2014-P", f: true },
  { issue: "2014-D", f: true },
  { issue: "2014-S, Proof" },
  { issue: "2013-P", f: true },
  { issue: "2013-D", f: true },
  { issue: "2013-S, Proof" },
  { issue: "2012-P", f: true },
  { issue: "2012-D", f: true },
  { issue: "2012-S, Proof" },
  { issue: "2011-P", f: true },
  { issue: "2011-D" },
  { issue: "2011-S, Proof" },
  { issue: "2010-P", f: true },
  { issue: "2010-D", f: true },
  { issue: "2010-S, Proof" },
  { issue: "2009-P" },
  { issue: "2009-D" },
  { issue: "2009-S, Proof" },
  { issue: "2008-P" },
  { issue: "2008-D", f: true },
  { issue: "2008-S, Proof" },
  { issue: "2007-P", f: true },
  { issue: "2007-D" },
  { issue: "2007-S, Proof" },
  { issue: "2006-P", f: true },
  { issue: "2006-D", f: true },
  { issue: "2006-S, Proof" },
];
</script>
