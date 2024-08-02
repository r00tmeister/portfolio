<template>
  <div class=" ">
    <ul class="flex justify-center content-center items-center font-mono">
      <li v-for="item in menu" :key="item.name" class="m-8">
        <nuxt-link :to="item.url" class="text-white">{{ item.name }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
const menu = ref([
  { name: 'Home', url: '/' },
  { name: 'About', url: '/about' },
  { name: 'Languages', url: '/languages' },
  { name: 'Projects', url: '/projects' },
])

</script>