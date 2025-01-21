<template>
    <div class="md:p-8 space-y-8 ">
        <LanguageTiles title="Front-end" :languages="languages" type="front-end" />
        <LanguageTiles title="Back-end" :languages="languages" type="back-end" />
        <LanguageTiles title="Database" :languages="languages" type="database" />
        <LanguageTiles title="Cloud" :languages="languages" type="cloud" />
        <LanguageTiles title="DevOps" :languages="languages" type="devops" />
        <LanguageTiles title="Testing" :languages="languages" type="testing" />
    </div>
</template>

<script lang="ts" setup>
import LanguageTiles from './LanguageTiles.vue';


const languages = ref([{ id: 0, name: 'HTML', type: 'front-end', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg', proficiency: 5, experience: 5 }, {
    id: 1,
    name: 'CSS',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg',
    proficiency: "5/5",
    experience: 5
}, {
    id: 2,
    name: 'JavaScript',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg',
    proficiency: "5/5",
    experience: 5
}, {
    id: 3,
    name: 'TypeScript',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg',
    proficiency: "3/5",
    experience: 1
},
{
    id: 3,
    name: 'TailwindCSS',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original-wordmark.svg',
    proficiency: "5/5",
    experience: 3
},
{
    id: 4,
    name: 'Vue.js',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original.svg',
    proficiency: "5/5",
    experience: 3
}, {
    id: 5,
    name: 'React.js',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg',
    proficiency: "3/5",
    experience: 2
}, {
    id: 6,
    name: 'NextJS',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg',
    proficiency: "3/5",
    experience: 1
}, {
    id: 7,
    name: 'NuxtJS',
    type: 'front-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nuxtjs/nuxtjs-original.svg',
    proficiency: "5/5",
    experience: 2
}, {
    id: 8,
    name: 'Node.js',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg',
    proficiency: "3/5",
    experience: 1
}, {
    id: 9,
    name: 'Python',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg',
    proficiency: "4/5",
    experience: 2
}, {
    id: 10,
    name: 'FastAPI',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/fastapi/fastapi-original.svg',
    proficiency: "5/5",
    experience: 2
}, {
    id: 11,
    name: 'C',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/c/c-original.svg',
    proficiency: "3/5",
    experience: 2
}, {
    id: 12,
    name: 'C++',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg',
    proficiency: "3/5",
    experience: 2
}, {
    id: 13,
    name: 'Java',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg',
    proficiency: "3/5",
    experience: 2
},
{
    id: 13,
    name: 'C#',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/csharp/csharp-original.svg',
    proficiency: "2/5",
    experience: 1
},
{
    id: 13,
    name: 'PHP',
    type: 'back-end',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/php/php-original.svg',
    proficiency: "3/5",
    experience: 2
},
    {
        id: 13,
        name: 'GraphQL',
        type: 'back-end',
        imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/graphql/graphql-plain.svg',
        proficiency: "3/5",
        experience: 1
    },
{
    id: 13,
    name: 'MySQL',
    type: 'database',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg',
    proficiency: "3/5",
    experience: 1
},
{
    id: 13,
    name: 'PostgreSQL',
    type: 'database',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg',
    proficiency: "3/5",
    experience: 2
},
{
    id: 13,
    name: 'Supabase',
    type: 'database',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/supabase/supabase-original.svg',
    proficiency: "2/5",
    experience: 1
},
{
    id: 13,
    name: 'Firebase',
    type: 'database',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/firebase/firebase-original.svg',
    proficiency: "2/5",
    experience: 1
},
{
    id: 13,
    name: 'DynamoDB',
    type: 'database',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/dynamodb/dynamodb-original.svg',
    proficiency: "3/5",
    experience: 1
},
{
    id: 13,
    name: 'Azure',
    type: 'cloud',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azure/azure-original.svg',
    proficiency: "4/5",
    experience: 2
},
{
    id: 13,
    name: 'AWS',
    type: 'cloud',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/amazonwebservices/amazonwebservices-original-wordmark.svg',
    proficiency: "2/5",
    experience: 1
},
{
    id: 13,
    name: 'Oracle',
    type: 'cloud',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/oracle/oracle-original.svg',
    proficiency: "1/5",
    experience: 1
},
    ,
{
    id: 13,
    name: 'Azure DevOps',
    type: 'devops',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azuredevops/azuredevops-original.svg',
    proficiency: "4/5",
    experience: 2
},
{
    id: 13,
    name: 'Github Actions',
    type: 'devops',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubactions/githubactions-original.svg',
    proficiency: "4/5",
    experience: 2
},
    ,
{
    id: 13,
    name: 'Vitest',
    type: 'testing',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vitest/vitest-original.svg',
    proficiency: "3/5",
    experience: 2
},
    ,
{
    id: 13,
    name: 'Cypress',
    type: 'testing',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cypressio/cypressio-original.svg',
    proficiency: "3/5",
    experience: 1
},
    ,
{
    id: 13,
    name: 'Pytest',
    type: 'testing',
    imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/pytest/pytest-original.svg',
    proficiency: "3/5",
    experience: 2
}

])
</script>

<style></style>
