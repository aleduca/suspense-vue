<template>
  <h2>Test</h2>
</template>
<script setup>
  import {reactive} from 'vue';
  const user = reactive({info:{}})

  async function getTeste(){
    return await new Promise(resolve => {
      setTimeout(() => {
        resolve('teste')
      }, 1200)
    })
  }

  user.info = await getTeste();
</script>