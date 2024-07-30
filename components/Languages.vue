<template>
    <div class="p-8 ">
        <LanguageSection title="Front-end Languages" :languages="languages" type="front-end" />
        <LanguageSection title="Back-end Languages" :languages="languages" type="back-end" />
        <LanguageSection title="Database" :languages="languages" type="database" />
    </div>
</template>

<script lang="ts" setup>

const languages = ref([{ id: 0, name: 'HTML', type: 'front-end', proficiency: 5, experience: 5 }, {
    id: 1,
    name: 'CSS',
    type: 'front-end',
    proficiency: 5,
    experience: 5
}, {
    id: 2,
    name: 'JavaScript',
    type: 'front-end',
    proficiency: 5,
    experience: 5
}, {
    id: 3,
    name: 'TypeScript',
    type: 'front-end',
    proficiency: 3,
    experience: 2
}, {
    id: 4,
    name: 'Vue.js',
    type: 'front-end',
    proficiency: 5,
    experience: 2
}, {
    id: 5,
    name: 'React.js',
    type: 'front-end',
    proficiency: 3,
    experience: 1
}, {
    id: 6,
    name: 'NextJS',
    type: 'front-end',
    proficiency: 3,
    experience: 1
}, {
    id: 7,
    name: 'NuxtJS',
    type: 'front-end',
    proficiency: 4,
    experience: 1
}, {
    id: 8,
    name: 'Node.js',
    type: 'back-end',
    proficiency: 5,
    experience: 5
}, {
    id: 9,
    name: 'Python',
    type: 'back-end',
    proficiency: 3,
    experience: 1
}, {
    id: 10,
    name: 'FastAPI',
    type: 'back-end',
    proficiency: 3,
    experience: 1
}, {
    id: 11,
    name: 'C',
    type: 'back-end',
    proficiency: 5,
    experience: 5
}, {
    id: 12,
    name: 'C++',
    type: 'back-end',
    proficiency: 5,
    experience: 5
}, {
    id: 13,
    name: 'Java',
    type: 'back-end',
    proficiency: 5,
    experience: 5
},
{
    id: 13,
    name: 'C#',
    type: 'back-end',
    proficiency: 5,
    experience: 5
},
{
    id: 13,
    name: 'MySQL',
    type: 'database',
    proficiency: 5,
    experience: 5
},
{
    id: 13,
    name: 'PostgreSQL',
    type: 'database',
    proficiency: 5,
    experience: 5
},
{
    id: 13,
    name: 'Supabase',
    type: 'database',
    proficiency: 5,
    experience: 5
},
{
    id: 13,
    name: 'Firebase',
    type: 'database',
    proficiency: 5,
    experience: 5
}])
</script>

<style></style>