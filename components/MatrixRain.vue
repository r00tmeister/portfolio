<template>
    <canvas ref="canvasRef" class="fixed top-0 left-0 w-full h-full z-[-1]"></canvas>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const canvasRef = ref(null)

onMounted(() => {
    const canvas = canvasRef.value
    const ctx = canvas.getContext('2d')
    const dpr = window.devicePixelRatio || 1
    const resizeCanvas = () => {
        const { width, height } = canvas.getBoundingClientRect()
        canvas.width = width * dpr
        canvas.height = (height) * dpr
        ctx.scale(dpr, dpr)
    }

    resizeCanvas()

    const columns = Math.floor(canvas.width / 10)
    const drops = Array(columns).fill(1)

    function draw() {
        ctx.fillStyle = 'rgba(0, 0, 0, 0.05)'
        ctx.fillRect(0, 0, canvas.width, canvas.height)
        ctx.fillStyle = '#0F0'
       /*  ctx.fillStyle = '#990F02' */
        ctx.font = '10px monospace'
        for (let i = 0; i < drops.length; i++) {
            const text = String.fromCharCode(1e2 + Math.random() * 33)
            ctx.fillText(text, i * 10, drops[i] * 10)
            if (drops[i] * 10 > canvas.height && Math.random() > 0.975) {
                drops[i] = 0
            }
            drops[i]++
        }
    }

    const intervalId = setInterval(draw, 42)

    window.addEventListener('resize', resizeCanvas)

    onBeforeUnmount(() => {
        clearInterval(intervalId)
        window.removeEventListener('resize', resizeCanvas)
    })
})
</script>