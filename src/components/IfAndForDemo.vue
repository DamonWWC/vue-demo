<script setup>
import { ref } from "vue";

const show = ref(true);
const list = ref([1, 2, 3, 4]);
</script>

<template>
  <div>
    <button @click="show = !show">Toggle List</button>
    <button @click="list.push(list.length + 1)">push number</button>
    <button @click="list.pop()">pop number</button>
    <button @click="list.reverse()">Reverse List</button>

    <ul v-if="show && list.length">
      <li v-for="item in list" >{{ item }}</li>
    </ul>
    <p v-else-if="list.length">List is empty, but hidden</p>
    <p v-else>List is Empty</p>
  </div>
</template>