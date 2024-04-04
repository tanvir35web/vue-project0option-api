<template>
  <nav class="border border-b-2 flex justify-between " 
  :class="{'bg-gray-900 text-white' : !useDarkNavBar, 'bg-white text-black' : useDarkNavBar}"
  >
    <ul class="flex">
      <li
        v-for="(page, index) in pages"
        :key="index"
        class="px-4 py-2 border-r-2 hover:bg-green-700 border-gray-700 font-medium cursor-pointer"
      >
        <a
          :href="page.link.url"
          :title="`This Link goes to the ${page.link.text} page`"
          @click.prevent="navLinkClick(index)"
          >{{ page.link.text }}</a
        >
      </li>
    </ul>
    <button @click.prevent="$emit('toggle-theme')" class="px-3 border-2 ">Theme Toggle</button>
  </nav>
</template>

<script>
export default {
  props: ['pages', 'activePage', 'navLinkClick', 'useDarkNavBar'],
}
</script>
