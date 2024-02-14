
<template>
 <div id="top" class="top">

  <p> You have {{ money }} $ </p>
 </div>
<div id="middle" class="middle">
 
  <p id="Q1"> {{ A }}</p>
  <button @click = "answer = true; "> True </button>       <button @click = "answer = false"> False</button>

  <p> answer is {{ answer }}</p>
   
</div>



</template>




<script setup>
import { ref } from 'vue'
let money = ref(0)
let answer = ref(null)




if (answer == true) {
  console.log('you got it right!')
}
else{

  console.log("what")
}




const A = 'One of the fundamental principles of casinos is that they are designed to have a mathematical advantage over players. This is known as the “house edge,” which ensures that the casino will statistically profit in the long run.'
</script>







<style scoped>

#top{
  color: rgb(0, 252, 34);
  
}

</style>


<!-- 
// use v if  to display data and change ui -->


