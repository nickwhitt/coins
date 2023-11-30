<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <ol class="flex gap-2 text-sm items-center">
        <li><NuxtLink to="/">Federal Issues</NuxtLink></li>
        <li><ChevronRightIcon class="w-4 h-4" /></li>
        <li>Dimes</li>
      </ol>
      <h1 class="text-3xl font-bold tracking-tight">Roosevelt Dimes</h1>
      <p>Since 1946</p>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 space-y-4">
    <Card>
      <template #header>Clad Coinage and Silver Proofs</template>
      <template #subheader>1965 to Date</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/roosevelt-2023p.webp"
              placeholder
              loading="lazy"
            />
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/roosevelt-clad-reverse.webp"
              placeholder
              loading="lazy"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Circulation strike
          </figcaption>
        </figure>
        <figure>
          <NuxtImg
            class="rounded-full w-24 h-24"
            src="/img/roosevelt-2023s.webp"
            placeholder
            loading="lazy"
          />
          <figcaption class="text-sm font-thin text-center">
            Proof strike
          </figcaption>
        </figure>
      </div>

      <div class="grid lg:grid-cols-2 gap-4">
        <CoinList :rows="clad" class="lg:hidden" />
        <CoinList
          :rows="clad.slice(0, Math.floor(clad.length / 2))"
          class="hidden lg:grid"
        />
        <CoinList
          :rows="clad.slice(Math.floor(clad.length / 2), clad.length)"
          class="hidden lg:grid"
        />
      </div>
    </Card>

    <Card>
      <template #header>Silver Coinage</template>
      <template #subheader>1946-1964</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/roosevelt-1951.webp"
              placeholder
              loading="lazy"
            />
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/roosevelt-silver-reverse.webp"
              placeholder
              loading="lazy"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Circulation strike
          </figcaption>
        </figure>
        <figure>
          <NuxtImg
            class="rounded-full w-24 h-24"
            src="/img/roosevelt-1951-proof.webp"
            placeholder
            loading="lazy"
          />
          <figcaption class="text-sm font-thin text-center">
            Proof strike
          </figcaption>
        </figure>
      </div>

      <div class="grid lg:grid-cols-2 gap-4">
        <CoinList :rows="silver" class="lg:hidden" />
        <CoinList
          :rows="silver.slice(0, Math.floor(silver.length / 2))"
          class="hidden lg:grid"
        />
        <CoinList
          :rows="silver.slice(Math.floor(silver.length / 2), silver.length)"
          class="hidden lg:grid"
        />
      </div>
    </Card>
  </main>

  <footer class="p-4"></footer>
</template>

<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";
const silver = [
  { issue: "1964" },
  { issue: "1964, Proof" },
  { issue: "1964-D" },
  { issue: "1963" },
  { issue: "1963, Proof" },
  { issue: "1963-D" },
  { issue: "1962" },
  { issue: "1962, Proof" },
  { issue: "1962-D" },
  { issue: "1961" },
  { issue: "1961, Proof" },
  { issue: "1961-D" },
  { issue: "1960" },
  { issue: "1960, Proof" },
  { issue: "1960-D" },
  { issue: "1959" },
  { issue: "1959, Proof" },
  { issue: "1959-D" },
  { issue: "1958" },
  { issue: "1958, Proof" },
  { issue: "1958-D" },
  { issue: "1957" },
  { issue: "1957, Proof" },
  { issue: "1957-D" },
  { issue: "1956" },
  { issue: "1956, Proof" },
  { issue: "1956-D" },
  { issue: "1955" },
  { issue: "1955, Proof" },
  { issue: "1955-D" },
  { issue: "1955-S" },
  { issue: "1954" },
  { issue: "1954, Proof" },
  { issue: "1954-D" },
  { issue: "1954-S" },
  { issue: "1953" },
  { issue: "1953, Proof" },
  { issue: "1953-D" },
  { issue: "1953-S" },
  { issue: "1952" },
  { issue: "1952, Proof" },
  { issue: "1952-D" },
  { issue: "1952-S" },
  { issue: "1951" },
  { issue: "1951, Proof" },
  { issue: "1951-D" },
  { issue: "1951-S" },
  { issue: "1950" },
  { issue: "1950, Proof" },
  { issue: "1950-D" },
  { issue: "1950-S" },
  { issue: "1949" },
  { issue: "1949-D" },
  { issue: "1949-S" },
  { issue: "1948" },
  { issue: "1948-D" },
  { issue: "1948-S" },
  { issue: "1947" },
  { issue: "1947-D" },
  { issue: "1947-S" },
  { issue: "1946" },
  { issue: "1946-D" },
  { issue: "1946-S" },
];
const clad = [
  { issue: "2023-P" },
  { issue: "2023-D" },
  { issue: "2023-S, Proof" },
  { issue: "2023-S, Proof, Silver" },
  { issue: "2022-P" },
  { issue: "2022-D" },
  { issue: "2022-S, Proof" },
  { issue: "2022-S, Proof, Silver" },
  { issue: "2021-P" },
  { issue: "2021-D" },
  { issue: "2021-S, Proof" },
  { issue: "2021-S, Proof, Silver" },
  { issue: "2020-P" },
  { issue: "2020-D" },
  { issue: "2020-S, Proof" },
  { issue: "2020-S, Proof, Silver" },
  { issue: "2019-P" },
  { issue: "2019-D" },
  { issue: "2019-S, Proof" },
  { issue: "2019-S, Proof, Silver" },
  { issue: "2018-P" },
  { issue: "2018-D" },
  { issue: "2018-S, Proof" },
  { issue: "2018-S, Proof, Silver" },
  { issue: "2017-P" },
  { issue: "2017-D" },
  { issue: "2017-S, Proof" },
  { issue: "2017-S, Proof, Silver" },
  { issue: "2016-P" },
  { issue: "2016-D" },
  { issue: "2016-S, Proof" },
  { issue: "2016-S, Proof, Silver" },
  { issue: "2015-P" },
  { issue: "2015-P, RevPf, Silver" },
  { issue: "2015-D" },
  { issue: "2015-S, Proof" },
  { issue: "2015-S, Proof, Silver" },
  { issue: "2015-W, Proof, Silver" },
  { issue: "2014-P" },
  { issue: "2014-D" },
  { issue: "2014-S, Proof" },
  { issue: "2014-S, Proof, Silver" },
  { issue: "2013-P" },
  { issue: "2013-D" },
  { issue: "2013-S, Proof" },
  { issue: "2013-S, Proof, Silver" },
  { issue: "2012-P" },
  { issue: "2012-D" },
  { issue: "2012-S, Proof" },
  { issue: "2012-S, Proof, Silver" },
  { issue: "2011-P" },
  { issue: "2011-D" },
  { issue: "2011-S, Proof" },
  { issue: "2011-S, Proof, Silver" },
  { issue: "2010-P" },
  { issue: "2010-D" },
  { issue: "2010-S, Proof" },
  { issue: "2010-S, Proof, Silver" },
  { issue: "2009-P" },
  { issue: "2009-D" },
  { issue: "2009-S, Proof" },
  { issue: "2009-S, Proof, Silver" },
  { issue: "2008-P" },
  { issue: "2008-D" },
  { issue: "2008-S, Proof" },
  { issue: "2008-S, Proof, Silver" },
  { issue: "2007-P" },
  { issue: "2007-D" },
  { issue: "2007-S, Proof" },
  { issue: "2007-S, Proof, Silver" },
  { issue: "2006-P" },
  { issue: "2006-D" },
  { issue: "2006-S, Proof" },
  { issue: "2006-S, Proof, Silver" },
  { issue: "2005-P" },
  { issue: "2005-P, RevPf, Silver" },
  { issue: "2005-D" },
  { issue: "2005-S, Proof" },
  { issue: "2005-S, Proof, Silver" },
  { issue: "2005-W, Proof, Silver" },
  { issue: "2004-P" },
  { issue: "2004-D" },
  { issue: "2004-S, Proof" },
  { issue: "2004-S, Proof, Silver" },
  { issue: "2003-P" },
  { issue: "2003-D" },
  { issue: "2003-S, Proof" },
  { issue: "2003-S, Proof, Silver" },
  { issue: "2002-P" },
  { issue: "2002-D" },
  { issue: "2002-S, Proof" },
  { issue: "2002-S, Proof, Silver" },
  { issue: "2001-P" },
  { issue: "2001-D" },
  { issue: "2001-S, Proof" },
  { issue: "2001-S, Proof, Silver" },
  { issue: "2000-P" },
  { issue: "2000-D" },
  { issue: "2000-S, Proof" },
  { issue: "2000-S, Proof, Silver" },
  { issue: "1999-P" },
  { issue: "1999-D" },
  { issue: "1999-S, Proof" },
  { issue: "1999-S, Proof, Silver" },
  { issue: "1998-P" },
  { issue: "1998-D" },
  { issue: "1998-S, Proof" },
  { issue: "1998-S, Proof, Silver" },
  { issue: "1997-P" },
  { issue: "1997-D" },
  { issue: "1997-S, Proof" },
  { issue: "1997-S, Proof, Silver" },
  { issue: "1996-P" },
  { issue: "1996-D" },
  { issue: "1996-S, Proof" },
  { issue: "1996-S, Proof, Silver" },
  { issue: "1996-W" },
  { issue: "1995-P" },
  { issue: "1995-P, RevPf, Silver" },
  { issue: "1995-D" },
  { issue: "1995-S, Proof" },
  { issue: "1995-S, Proof, Silver" },
  { issue: "1995-W, Proof, Silver" },
  { issue: "1994-P" },
  { issue: "1994-D" },
  { issue: "1994-S, Proof" },
  { issue: "1994-S, Proof, Silver" },
  { issue: "1993-P" },
  { issue: "1993-D" },
  { issue: "1993-S, Proof" },
  { issue: "1993-S, Proof, Silver" },
  { issue: "1992-P" },
  { issue: "1992-D" },
  { issue: "1992-S, Proof" },
  { issue: "1992-S, Proof, Silver" },
  { issue: "1991-P" },
  { issue: "1991-D" },
  { issue: "1991-S, Proof" },
  { issue: "1990-P" },
  { issue: "1990-D" },
  { issue: "1990-S, Proof" },
  { issue: "1989-P" },
  { issue: "1989-D" },
  { issue: "1989-S, Proof" },
  { issue: "1988-P" },
  { issue: "1988-D" },
  { issue: "1988-S, Proof" },
  { issue: "1987-P" },
  { issue: "1987-D" },
  { issue: "1987-S, Proof" },
  { issue: "1986-P" },
  { issue: "1986-D" },
  { issue: "1986-S, Proof" },
  { issue: "1985-P" },
  { issue: "1985-D" },
  { issue: "1985-S, Proof" },
  { issue: "1984-P" },
  { issue: "1984-D" },
  { issue: "1984-S, Proof" },
  { issue: "1983-P" },
  { issue: "1983-D" },
  { issue: "1983-S, Proof" },
  { issue: "1982-P" },
  { issue: "1982-D" },
  { issue: "1982-S, Proof" },
  { issue: "1981-P" },
  { issue: "1981-D" },
  { issue: "1981-S, Proof" },
  { issue: "1980-P" },
  { issue: "1980-D" },
  { issue: "1980-S, Proof" },
  { issue: "1979" },
  { issue: "1979-D" },
  { issue: "1979-S, Proof" },
  { issue: "1978" },
  { issue: "1978-D" },
  { issue: "1978-S, Proof" },
  { issue: "1977" },
  { issue: "1977-D" },
  { issue: "1977-S, Proof" },
  { issue: "1976" },
  { issue: "1976-D" },
  { issue: "1976-S, Proof" },
  { issue: "1975" },
  { issue: "1975-D" },
  { issue: "1975-S, Proof" },
  { issue: "1974" },
  { issue: "1974-D" },
  { issue: "1974-S, Proof" },
  { issue: "1973" },
  { issue: "1973-D" },
  { issue: "1973-S, Proof" },
  { issue: "1972" },
  { issue: "1972-D" },
  { issue: "1972-S, Proof" },
  { issue: "1971" },
  { issue: "1971-D" },
  { issue: "1971-S, Proof" },
  { issue: "1970" },
  { issue: "1970-D" },
  { issue: "1970-S, Proof" },
  { issue: "1969" },
  { issue: "1969-D" },
  { issue: "1969-S, Proof" },
  { issue: "1968" },
  { issue: "1968-D" },
  { issue: "1968-S, Proof" },
  { issue: "1967" },
  { issue: "1966" },
  { issue: "1965" },
];
</script>
