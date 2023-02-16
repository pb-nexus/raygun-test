<template>
  <div>
    <button @click="hello">Hello</button>
    <button @click="error">Error</button>
  </div>
</template>

<script setup lang="ts">

function hello(){
  console.log('Hello');
}
function error(){
  console.log(a);
}
</script>