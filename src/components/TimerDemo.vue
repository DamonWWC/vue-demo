<script setup>
import { ref, onUnmounted } from 'vue'

const duration = ref(15 * 1000)
const elapsed = ref(0)

let lastTime = performance.now()
let handle
const update = () => {
    const time = performance.now()
    elapsed.value += Math.min(time - lastTime, duration.value - elapsed.value)
    lastTime = time
    handle = requestAnimationFrame(update)
}

update()
onUnmounted(() => {
    cancelAnimationFrame(handle)
})

</script>
<template>
    <label>Elapsed Time:<progress :value="elapsed / duration"></progress>
    </label>
    <div>{{ (elapsed / 1000).toFixed(1) }}s</div>

    <div>
        Duration:<input type="range" v-model="duration" min="1" max="30000">
        {{ (duration / 1000).toFixed(1) }}s
    </div>
    <button @click="elapsed = 0">Reset</button>
</template>
<style scoped>
.elapsed-container {
    width: 1000px;
}

.elapsed-bar {
    background-color: yellow;
    height: 10px;
}
label{
    white-space: nowrap;
}
</style>