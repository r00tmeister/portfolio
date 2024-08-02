<template>
  <div class="hidden md:flex items-center justify-center">
    <ul class="flex justify-center content-center items-center font-mono">
      <li v-for="item in menu" :key="item.name" class="m-8 ">
        <nuxt-link :to="item.url" class="text-white ">{{ item.name }}</nuxt-link>
      </li>
    </ul>
  </div>
  <div class="md:hidden">
    <ul class="flex flex-col justify-center content-center items-center font-mono">
      <li class="m-8 self-end" @click="burgerMenu = !burgerMenu">
        <Bars4Icon class="h-8 w-8 text-white" />
      </li>
      <li v-for="item in menu" :key="item.name" class="m-8 flex flex-col" v-if="burgerMenu"
        @click="burgerMenu = !burgerMenu">
        <nuxt-link :to="item.url" class="text-white ">{{ item.name }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
import { Bars4Icon } from '@heroicons/vue/20/solid';
const burgerMenu = ref(false)
const menu = ref([
  { name: 'Home', url: '/' },
  { name: 'About', url: '/about' },
  { name: 'Languages', url: '/languages' },
  { name: 'Projects', url: '/projects' },
])

</script>