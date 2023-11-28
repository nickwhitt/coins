<template>
  <article class="border sm:rounded-lg break-inside-avoid-column bg-white">
    <hgroup class="px-6 py-2 border-b">
      <h2 class="text-xl font-bold"><slot name="header">Foo</slot></h2>
      <p><slot name="subheader">Bar</slot></p>
    </hgroup>
    <div class="px-6 py-2">
      <slot><CoinList /></slot>
    </div>
  </article>
</template>
