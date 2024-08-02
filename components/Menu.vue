<template>
  <div class="hidden md:flex items-center justify-center">
    <ul class="flex justify-center content-center items-center font-mono">
      <li v-for="item in menu" :key="item.name" class="m-8 ">
        <nuxt-link :to="item.url" class="text-white font-mono">{{ item.name }}</nuxt-link>
      </li>
    </ul>
  </div>
  <div class="md:hidden "
    :class="burgerMenu ? 'bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg h-screen w-full z-[11]' : ''">
    <ul class="flex flex-col justify-center content-center items-center font-mono">
      <li class="m-8 self-end" @click="burgerMenu = !burgerMenu">
        <Bars4Icon class="h-8 w-8 text-white font-mono" />
      </li>
      <TransitionGroup name="list">
        <li v-for="item in menu" :key="item.name" class="m-8 flex flex-col" v-if="burgerMenu"
          @click="burgerMenu = !burgerMenu">
          <nuxt-link :to="item.url" class="text-white font-mono">{{ item.name }}</nuxt-link>
        </li>
      </TransitionGroup>
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
<style>

.list-enter-active{
  transition: all 0.5s ease;
}

.list-leave-active {
  transition: all 0.1s ease;
}



.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(30px);
}</style>