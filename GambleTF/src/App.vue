
<template>
 <div id="top" class="middle">

  <p> You have X amonut of dollars you gambler</p>
 </div>
<div id="middle" class="middle">
 
  <p id="Q1">One of the fundamental principles of casinos is that they are designed to have a mathematical advantage over players. This is known as the “house edge,” which ensures that the casino will statistically profit in the long run.</p>
  <button @click = "answer.push('testwork')"> True </button> <button> False</button>

  <p> answer is {{ answer }}</p>

</div>



</template>




<script setup>
import { ref } from 'vue'
const money = ref(0)
const answer = ref([])
</script>



<style scoped>

.top{
  color: blue;
}

</style>


<!-- 
// use v if  to display data and change ui -->


