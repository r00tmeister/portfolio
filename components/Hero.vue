<template>
  <div class="flex flex-col justify-center md:h-96 items-center space-y-12 text-wrap ">
    <h1 class="text-white text-xl md:text-5xl font-bold font-mono text-center"> {{ props.heading }}</h1>
    <h3 class="text-white px-8 text-md md:text-2xl font-bold font-mono text-center ">{{ props.subHeading }}</h3>
    <NuxtLink :to="props.buttonLink">
      <button
        class="hover:bg-black-700 text-white font-bold py-2 px-4 rounded-lg border-2 border-solid border-white  flex items-center space-x-2">
        <span class="opacity-none animate-pulse " v-if="props.button">{{ props.buttonText }} </span>
        <nuxt-icon name="buttons/whiteRabbit" class="animate-bounce text-lg font-bold"></nuxt-icon>
      </button>
    </NuxtLink>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  heading: String,
  subHeading: String,
  button: Boolean,
  buttonText: String,
  buttonSVG: String,
  buttonLink: String
})

</script>

<style>

</style>