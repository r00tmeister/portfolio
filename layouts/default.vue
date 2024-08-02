<template>
    <MatrixRain class="fixed inset-0 h-full z-[-1]"></MatrixRain>
    <div class="md:relative min-h-screen overflow-hidden z-10 font-mono">
        <Menu class="absolute z-[11]"></Menu>
        <slot></slot>
        <Footer></Footer>
    </div>
</template>

<script lang="ts" setup>

</script>

<style>

</style>