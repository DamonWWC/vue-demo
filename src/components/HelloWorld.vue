<template>
<div>
 <h1>{{message}}</h1>

 <button @click="reverseMessage">Resverse Message</button>

 <button @click="message+='!'">Append "!"</button>

 <a href="https://vuejs.org" @click.prevent="notify"> A link with e.preventDefault</a>
 </div>
</template>

<script setup>

import {ref} from "vue"

const message=ref("hello world")

function reverseMessage(){
  message.value=message.value.split('').reverse().join('')
}

function notify(){
  alert('navigation was prevented.')
}

</script>

<style scoped>
button,a{
  display: block;
  margin-bottom: 1em;
}
button{
  margin-left: auto;
}
</style>

