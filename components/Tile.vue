<template>
    <div class=" flex  rounded-md p-4 bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg">
        <div class="flex flex-col items-start justify-start h-full ">
            <h1 class="text-2xl font-mono font-bold text-white">{{ prop.name }}</h1>
            <p class="text-sm text-green-400 font-bold mb-4">{{ prop.type }}</p>
            <img :src="prop.imageUrl" alt="" class="w-8 h-8 mb-6 rounded-full">
            <p class="text-sm text-gray-400">Proficiency: {{ prop.proficiency }}</p>
            <p class="text-sm text-gray-400">Experience: {{ prop.experience }} years</p>
        </div>
    </div>
</template>
<script lang="ts" setup>
const prop = defineProps({
    name: String,
    type: String,
    proficiency: Number,
    experience: Number,
    imageUrl: String
})
</script>

<style></style>