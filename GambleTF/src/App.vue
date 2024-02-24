
<template>
 <div id="top" class="top">

  <p> You have {{ money }} $ </p>
 </div>
<div id="middle" class="middle">
 
  <p id="Q1"> {{ A }}</p>
  <button class="Button1" @click = "answer = true; listofanswer.pop(); listofanswer.push(answer);  "> True </button>  
  <button class="Button2" @click = "answer = false; listofanswer.pop(); listofanswer.push(answer);"> False</button>
  <br>
  <button class="Sumbit" @click=" console.log(listofanswer);      ">Submit</button>
  <p> answer is {{ answer }}</p>
   
</div>



</template>

<!-- diable buttons after sumbit is clicked
finsish making base funtion of true and false and get it wokring

finsihs writing this list on what to do and how

-->


<script setup>
import { ref } from 'vue'
let money = ref(0)
let answer = ref(null)
const listofanswer = [];






const A = 'One of the fundamental principles of casinos is that they are designed to have a mathematical advantage over players. This is known as the “house edge,” which ensures that the casino will statistically profit in the long run.'
</script>







<style scoped>

#top{
  color: rgb(0, 252, 34);
  
}

.Button1:active{
  background-color: hsl(108, 85%, 48%);
}
.Button2:active{
  background-color: rgb(255, 2, 2);
}


</style>


<!-- 
// use v if  to display data and change ui -->


