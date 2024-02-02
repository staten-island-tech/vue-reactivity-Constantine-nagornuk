<template>
  <div>


    <h1 v-if="answer">Correct</h1>
    <h1 v-else>Incorrect</h1>
  </div>
</template>

<script setup>
  const answer = true
  
</script>

<style lang="scss" scoped>

</style>

