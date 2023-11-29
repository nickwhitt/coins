<template>
  <Body class="bg-gray-100" />

  <div class="container mx-auto px-4">
    <hgroup class="py-8">
      <h1 class="text-3xl font-bold tracking-tight">Jefferson Nickels</h1>
    </hgroup>
  </div>

  <main class="container mx-auto sm:px-4 lg:columns-2 space-y-4">
    <Card>
      <template #header>Jefferson, Modified</template>
      <template #subheader>since 2006</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-2023p.webp"
            />
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-modified-reverse.webp"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Circulation strike
          </figcaption>
        </figure>
        <figure>
          <NuxtImg
            class="rounded-full w-24 h-24"
            src="/img/jefferson-2023s.webp"
          />
          <figcaption class="text-sm font-thin text-center">
            Proof strike
          </figcaption>
        </figure>
      </div>

      <CoinList :rows="modified" />
    </Card>

    <Card>
      <template #header>Westward Journey</template>
      <template #subheader>2004-2005</template>

      <div class="py-2 flex justify-evenly">
        <div class="grid grid-cols-2 gap-2 max-w-fit">
          <figure class="col-span-2 mx-auto">
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-2004p.webp"
            />
            <figcaption class="text-sm font-thin text-center">2004</figcaption>
          </figure>
          <figure>
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-la-purchase.webp"
            />
            <figcaption class="text-sm font-thin text-center">
              Peace<br />Medal
            </figcaption>
          </figure>
          <figure>
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-keelboat.webp"
            />
            <figcaption class="text-sm font-thin text-center">
              Keelboat
            </figcaption>
          </figure>
        </div>

        <div class="grid grid-cols-2 gap-2 max-w-fit">
          <figure class="col-span-2 mx-auto">
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-2005p.webp"
            />
            <figcaption class="text-sm font-thin text-center">2005</figcaption>
          </figure>
          <figure>
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-bison.webp"
            />
            <figcaption class="text-sm font-thin text-center">
              American<br />Bison
            </figcaption>
          </figure>
          <figure>
            <NuxtImg
              class="rounded-full w-24 h-24"
              src="/img/jefferson-ocean.webp"
            />
            <figcaption class="text-sm font-thin text-center">
              Ocean<br />In View!
            </figcaption>
          </figure>
        </div>
      </div>

      <CoinList :rows="westward" />
    </Card>

    <Card>
      <template #header>Wartime Silver Alloy</template>
      <template #subheader>1942-1945</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure>
          <div class="flex gap-1">
            <NuxtImg
              src="/img/jefferson-1944p-reverse.webp"
              class="rounded-full w-24 h-24"
            />
            <NuxtImg
              src="/img/jefferson-1943d-reverse.webp"
              class="rounded-full w-24 h-24"
            />
            <NuxtImg
              src="/img/jefferson-1942s-reverse.webp"
              class="rounded-full w-24 h-24"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Mintmark above Monticello
          </figcaption>
        </figure>
      </div>

      <CoinList :rows="wartime" />
    </Card>

    <Card>
      <template #header>Monticello Reverse</template>
      <template #subheader>1938-1942; 1946-2003</template>

      <div class="flex gap-4 py-2 justify-center">
        <figure class="">
          <div class="flex gap-1">
            <NuxtImg
              src="/img/jefferson-1940d.webp"
              class="rounded-full w-24 h-24"
            />
            <NuxtImg
              src="/img/jefferson-monticello-reverse.webp"
              class="rounded-full w-24 h-24"
            />
          </div>
          <figcaption class="text-sm font-thin text-center">
            Circulation strike
          </figcaption>
        </figure>
        <figure>
          <NuxtImg
            class="rounded-full w-24 h-24"
            src="/img/jefferson-1968s.webp"
          />
          <figcaption class="text-sm font-thin text-center">
            Proof strike
          </figcaption>
        </figure>
      </div>

      <CoinList :rows="monticello" />
    </Card>
  </main>

  <footer class="p-4"></footer>
</template>

<script setup>
const monticello = [
  { issue: "2003-P", cir: true },
  { issue: "2003-D", cir: true },
  { issue: "2003-S, Proof" },
  { issue: "2002-P", cir: true },
  { issue: "2002-D", cir: true },
  { issue: "2002-S, Proof" },
  { issue: "2001-P", cir: true },
  { issue: "2001-D", cir: true },
  { issue: "2001-S, Proof" },
  { issue: "2000-P", cir: true },
  { issue: "2000-D", cir: true },
  { issue: "2000-S, Proof" },
  { issue: "1999-P", cir: true },
  { issue: "1999-D", cir: true },
  { issue: "1999-S, Proof" },
  { issue: "1998-P", cir: true },
  { issue: "1998-D", cir: true },
  { issue: "1998-S, Proof" },
  { issue: "1997-P", cir: true },
  { issue: "1997-D" },
  { issue: "1997-S, Proof" },
  { issue: "1996-P", cir: true },
  { issue: "1996-D", cir: true },
  { issue: "1996-S, Proof" },
  { issue: "1995-P", cir: true },
  { issue: "1995-D", cir: true },
  { issue: "1995-S, Proof" },
  { issue: "1994-P", cir: true },
  { issue: "1994-D", cir: true },
  { issue: "1994-S, Proof" },
  { issue: "1993-P", cir: true },
  { issue: "1993-D", cir: true },
  { issue: "1993-S, Proof" },
  { issue: "1992-P", cir: true },
  { issue: "1992-D", cir: true },
  { issue: "1992-S, Proof" },
  { issue: "1991-P", cir: true },
  { issue: "1991-D", cir: true },
  { issue: "1991-S, Proof" },
  { issue: "1990-P", cir: true },
  { issue: "1990-D", cir: true },
  { issue: "1990-S, Proof" },
  { issue: "1989-P", cir: true },
  { issue: "1989-D", cir: true },
  { issue: "1989-S, Proof" },
  { issue: "1988-P", cir: true },
  { issue: "1988-D", cir: true },
  { issue: "1988-S, Proof" },
  { issue: "1987-P", cir: true },
  { issue: "1987-D", cir: true },
  { issue: "1987-S, Proof" },
  { issue: "1986-P", cir: true },
  { issue: "1986-D", cir: true },
  { issue: "1986-S, Proof" },
  { issue: "1985-P", cir: true },
  { issue: "1985-D", cir: true },
  { issue: "1985-S, Proof" },
  { issue: "1984-P", cir: true },
  { issue: "1984-D", cir: true },
  { issue: "1984-S, Proof" },
  { issue: "1983-P", cir: true },
  { issue: "1983-D", cir: true },
  { issue: "1983-S, Proof" },
  { issue: "1982-P", cir: true },
  { issue: "1982-D", cir: true },
  { issue: "1982-S, Proof" },
  { issue: "1981-P", cir: true },
  { issue: "1981-D", cir: true },
  { issue: "1981-S, Proof" },
  { issue: "1980-P", cir: true },
  { issue: "1980-D", cir: true },
  { issue: "1980-S, Proof" },
  { issue: "1979", cir: true },
  { issue: "1979-D", cir: true },
  { issue: "1979-S, Proof" },
  { issue: "1978", cir: true },
  { issue: "1978-D", cir: true },
  { issue: "1978-S, Proof" },
  { issue: "1977", cir: true },
  { issue: "1977-D", cir: true },
  { issue: "1977-S, Proof" },
  { issue: "1976", cir: true },
  { issue: "1976-D", cir: true },
  { issue: "1976-S, Proof" },
  { issue: "1975", cir: true },
  { issue: "1975-D", cir: true },
  { issue: "1975-S, Proof" },
  { issue: "1974", cir: true },
  { issue: "1974-D", cir: true },
  { issue: "1974-S, Proof" },
  { issue: "1973", cir: true },
  { issue: "1973-D", cir: true },
  { issue: "1973-S, Proof" },
  { issue: "1972", cir: true },
  { issue: "1972-D", cir: true },
  { issue: "1972-S, Proof" },
  { issue: "1971", cir: true },
  { issue: "1971-D", cir: true },
  { issue: "1971-S, Proof" },
  { issue: "1970-D", cir: true },
  { issue: "1970-S", cir: true },
  { issue: "1970-S, Proof" },
  { issue: "1969-D", cir: true },
  { issue: "1969-S", cir: true },
  { issue: "1969-S, Proof" },
  { issue: "1968-D", cir: true },
  { issue: "1968-S", cir: true },
  { issue: "1968-S, Proof" },
  { issue: "1967", cir: true },
  { issue: "1966", cir: true },
  { issue: "1965", cir: true },
  { issue: "1964", cir: true },
  { issue: "1964, Proof" },
  { issue: "1964-D", cir: true },
  { issue: "1963", cir: true },
  { issue: "1963, Proof" },
  { issue: "1963-D", cir: true },
  { issue: "1962", cir: true },
  { issue: "1962, Proof" },
  { issue: "1962-D", cir: true },
  { issue: "1961", cir: true },
  { issue: "1961, Proof" },
  { issue: "1961-D", cir: true },
  { issue: "1960", cir: true },
  { issue: "1960, Proof" },
  { issue: "1960-D", cir: true },
  { issue: "1959", cir: true },
  { issue: "1959, Proof" },
  { issue: "1959-D", cir: true },
  { issue: "1958", cir: true },
  { issue: "1958, Proof" },
  { issue: "1958-D", cir: true },
  { issue: "1957", cir: true },
  { issue: "1957, Proof" },
  { issue: "1957-D", cir: true },
  { issue: "1956", cir: true },
  { issue: "1956, Proof" },
  { issue: "1956-D", cir: true },
  { issue: "1955", cir: true },
  { issue: "1955, Proof" },
  { issue: "1955-D", cir: true },
  { issue: "1954", cir: true },
  { issue: "1954, Proof" },
  { issue: "1954-D", cir: true },
  { issue: "1954-S", cir: true },
  { issue: "1953", cir: true },
  { issue: "1953, Proof" },
  { issue: "1953-D", cir: true },
  { issue: "1953-S", cir: true },
  { issue: "1952", cir: true },
  { issue: "1952, Proof" },
  { issue: "1952-D", cir: true },
  { issue: "1952-S", cir: true },
  { issue: "1951", cir: true },
  { issue: "1951, Proof" },
  { issue: "1951-D", cir: true },
  { issue: "1951-S", cir: true },
  { issue: "1950", cir: true },
  { issue: "1950, Proof" },
  { issue: "1950-D" },
  { issue: "1949", cir: true },
  { issue: "1949-D", cir: true },
  { issue: "1949-S", cir: true },
  { issue: "1948", cir: true },
  { issue: "1948-D", cir: true },
  { issue: "1948-S", cir: true },
  { issue: "1947", cir: true },
  { issue: "1947-D", cir: true },
  { issue: "1947-S", cir: true },
  { issue: "1946", cir: true },
  { issue: "1946-D", cir: true },
  { issue: "1946-S", cir: true },
  { issue: "1942", cir: true },
  { issue: "1942, Proof" },
  { issue: "1942-D", cir: true },
  { issue: "1941", cir: true },
  { issue: "1941, Proof" },
  { issue: "1941-D", cir: true },
  { issue: "1941-S", cir: true },
  { issue: "1940", cir: true },
  { issue: "1940, Proof" },
  { issue: "1940-D", cir: true },
  { issue: "1940-S", cir: true },
  { issue: "1939", cir: true },
  { issue: "1939, Proof" },
  { issue: "1939-D" },
  { issue: "1939-S" },
  { issue: "1938", cir: true },
  { issue: "1938, Proof" },
  { issue: "1938-D", cir: true },
  { issue: "1938-S" },
];
const wartime = [
  { issue: "1945-P", cir: true },
  { issue: "1945-D", cir: true },
  { issue: "1945-S", cir: true },
  { issue: "1944-P", cir: true },
  { issue: "1944-D", cir: true },
  { issue: "1944-S", cir: true },
  { issue: "1943-P", cir: true },
  { issue: "1943-D", cir: true },
  { issue: "1943-S", cir: true },
  { issue: "1942-P", cir: true },
  { issue: "1942-P, Proof" },
  { issue: "1942-S", cir: true },
];
const westward = [
  { issue: "2005-P, American Bison", cir: true },
  { issue: "2005-D, American Bison" },
  { issue: "2005-S, American Bison, Proof" },
  { issue: "2005-P, Ocean in View", cir: true },
  { issue: "2005-D, Ocean in View" },
  { issue: "2005-S, Ocean in View, Proof" },
  { issue: "2004-P, Peace Medal" },
  { issue: "2004-D, Peace Medal", cir: true },
  { issue: "2004-S, Peace Medal, Proof" },
  { issue: "2004-P, Keelboat", cir: true },
  { issue: "2004-D, Keelboat", cir: true },
  { issue: "2004-S, Keelboat, Proof" },
];
const modified = [
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
