<template>
    <div>
        <h1 class="text-white"> {{ title }}</h1>
        <div class="flex flex-wrap">
            <div class=" m-4" v-for="language in filteredLanguages" key="language.id">
                <Tile :name="language.name" :type="language.type" :proficiency="language.proficiency"
                    :experience="language.experience" class="hover:cursor-pointer"></Tile>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { defineProps } from 'vue'
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