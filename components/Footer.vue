<template>
    <div class="flex fixed inset-x-0 bottom-0">
        <div class=" items-center flex flex-col space-x-8 p-4 ">
            <ul class="flex space-x-6">
                <NuxtLink to="https://www.linkedin.com/in/christiaan-johannes-n-50643153/">
                    <li class="text-white font-mono flex items-center"><nuxt-icon
                            name="social/linkedin"></nuxt-icon><span>LinkedIn</span> </li>
                </NuxtLink>
                <NuxtLink to="https://github.com/r00tmeister">
                    <li class="text-white font-mono flex items-center"><nuxt-icon name="social/github"></nuxt-icon><span
                            class="opacity-100">Github</span> </li>
                </NuxtLink>
            </ul>
        </div>
    </div>
</template>

<script lang="ts" setup>

</script>