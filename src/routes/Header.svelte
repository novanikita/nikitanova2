<script>
  import { page } from '$app/stores';

  $: ariaCurrent = (/** @type {string} */ currUrl) => ($page.url.pathname === currUrl ? 'page' : undefined);
</script>

<template lang="pug">
//- header.ids__wrapper.main-wrapper
//-   nav
//-     ul
//-       li
//-         a(aria-current!='{ ariaCurrent("/") }', href="/") Main

</template>

<style lang="postcss">
  ul {
    display: flex;
    list-style: none;
    gap: .5em;
  }

  a[aria-current='page'] {
    border-bottom: none;
    color: black;

    &:hover {
      color: black;
      cursor: default;
    }
  }
</style>
