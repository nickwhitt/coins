<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <h1 class="text-3xl font-bold tracking-tight">Jefferson Nickels</h1>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 lg:columns-2 space-y-4">
    <Card>
      <template #header>Modified Portrait</template>
      <template #subheader>since 2006</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-20 h-20"
              src="/img/jefferson-2023p.webp"
            />
            <NuxtImg
              class="rounded-full w-20 h-20"
              src="/img/jefferson-modified-reverse.webp"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Circulation strike
          </figcaption>
        </figure>
        <figure>
          <NuxtImg
            class="rounded-full w-20 h-20"
            src="/img/jefferson-2023s.webp"
          />
          <figcaption class="text-sm font-thin text-center">
            Proof strike
          </figcaption>
        </figure>
      </div>

      <CoinList :rows="coins" />
    </Card>

    <Card>
      <template #header>Westward Journey</template>
      <template #subheader>2004-2005</template>
    </Card>
    <Card>
      <template #header>Wartime Silver Alloy</template>
      <template #subheader>1942-1945</template>
    </Card>
    <Card>
      <template #header>Monticello Reverse</template>
      <template #subheader>1938-1942; 1946-2003</template>
    </Card>
  </main>

  <footer class="p-4"></footer>
</template>

<script setup>
const grades = ["cir", "unc", "pf"];
const coins = [
  { issue: "2023-P", cir: true },
  { issue: "2023-D" },
  { issue: "2023-S, Proof" },
  { issue: "2022-P", cir: true },
  { issue: "2022-D" },
  { issue: "2022-S, Proof" },
  { issue: "2021-P", cir: true },
  { issue: "2021-D", cir: true },
  { issue: "2021-S, Proof" },
  { issue: "2020-P", cir: true },
  { issue: "2020-D", cir: true },
  { issue: "2020-S, Proof" },
  { issue: "2019-P", cir: true },
  { issue: "2019-D", cir: true },
  { issue: "2019-S, Proof" },
  { issue: "2018-P", cir: true },
  { issue: "2018-D", cir: true },
  { issue: "2018-S, Proof" },
  { issue: "2017-P", cir: true },
  { issue: "2017-D", cir: true },
  { issue: "2017-S, Proof" },
  { issue: "2016-P", cir: true },
  { issue: "2016-D", cir: true },
  { issue: "2016-S, Proof" },
  { issue: "2015-P", cir: true },
  { issue: "2015-D", cir: true },
  { issue: "2015-S, Proof" },
  { issue: "2014-P", cir: true },
  { issue: "2014-D", cir: true },
  { issue: "2014-S, Proof" },
  { issue: "2013-P", cir: true },
  { issue: "2013-D", cir: true },
  { issue: "2013-S, Proof" },
  { issue: "2012-P", cir: true },
  { issue: "2012-D", cir: true },
  { issue: "2012-S, Proof" },
  { issue: "2011-P", cir: true },
  { issue: "2011-D" },
  { issue: "2011-S, Proof" },
  { issue: "2010-P", cir: true },
  { issue: "2010-D", cir: true },
  { issue: "2010-S, Proof" },
  { issue: "2009-P" },
  { issue: "2009-D" },
  { issue: "2009-S, Proof" },
  { issue: "2008-P" },
  { issue: "2008-D", cir: true },
  { issue: "2008-S, Proof" },
  { issue: "2007-P", cir: true },
  { issue: "2007-D" },
  { issue: "2007-S, Proof" },
  { issue: "2006-P", cir: true },
  { issue: "2006-D", cir: true },
  { issue: "2006-S, Proof" },
];
</script>
