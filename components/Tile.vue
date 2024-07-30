<template>
    <div class=" flex  rounded-md p-4 bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg">
        <div class="flex flex-col items-start justify-start h-full ">
            <h1 class="text-2xl font-bold text-white">{{ prop.name }}</h1>
            <p class="text-sm text-green-400 font-bold mb-4">{{ prop.type }}</p>
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
})
</script>

<style></style>