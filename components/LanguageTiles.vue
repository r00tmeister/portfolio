<template>
    <div class="flex flex-col items-center justify-center space-y-8">
        <h1 class="text-white text-2xl font-bold"> {{ title }}</h1>
        <div class="flex flex-wrap items-center justify-center">
            <div class=" md:m-4" v-for="language in filteredLanguages" key="language.id">
                <Tile :name="language.name" :type="language.type" :proficiency="language.proficiency"
                    :experience="language.experience" :imageUrl="language.imageUrl" class="hover:cursor-pointer"></Tile>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import Tile from './Tile.vue'
import { computed } from 'vue';

const props = defineProps({
    title: String,
    languages: Array,
    type: String
})

const filteredLanguages = computed(() => {
    return props.languages.filter((language) => language.type == props.type)
})
</script>

<style></style>