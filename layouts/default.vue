<template>
    <MatrixRain class="fixed inset-0 h-full z-[-1]"></MatrixRain>
    <div class="min-h-screen overflow-hidden z-10 font-mono">
        <Menu class="fixed top-0 left-0 z-[100]"></Menu>
        <div class="relative">
            <slot class="absolute"></slot>
        </div>
        <Footer></Footer>
    </div>
</template>

<script lang="ts" setup>

</script>