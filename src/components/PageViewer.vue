<template>
  <div class="flex flex-col items-center mt-52">
    <h1>{{ page.pageTitle }}</h1>
    <p>{{ page.content }}</p>
  </div>
</template>

<script>
export default {
  props: ['page']
}
</script>
