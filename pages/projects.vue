<template>
    <Hero heading="Projects" subHeading="Work history with grouped projects" :button='true'
        buttonText="The woman in the red dress" buttonSVG="buttons/redDress"
        buttonLink="https://www.youtube.com/watch?v=xvFZjo5PgG0" class=""></Hero>
    <ProjectsTimeline></ProjectsTimeline>
</template>

<script lang="ts" setup>
definePageMeta({
    layout: 'default'
})
</script>

<style></style>