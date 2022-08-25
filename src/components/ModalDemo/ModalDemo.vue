<script setup>
import modal from './Modal.vue'
import {ref} from 'vue'

const showModal=ref(false)

</script>
<template>
    <button id="show-modal" @click="showModal=true">Show Modal</button>

    <teleport to="body">
        <modal :show="showModal" @close="showModal=false">
        <template #header>
            <h3>custom header</h3>
        </template>
        </modal>
    </teleport>
</template>