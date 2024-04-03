<template>
  <nav class="border border-b-2">
    <ul class="flex">
      <li v-for="page in pages" class="text-red-800 hover:bg-red-100 px-4 py-2 font-medium cursor-pointer">
        <a>{{ page.link.text }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: ['pages']
}
</script>
