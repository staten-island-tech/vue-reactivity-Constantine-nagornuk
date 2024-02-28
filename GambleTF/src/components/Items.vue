<template>
    <div class="items-container">
      <h2 id="StoreTitle">Clothes</h2>
      <ul id="STUFF" class="STUFF">
        <li v-for="item in items" :key="item.id">
          {{ item.name }} <span>${{ item.price }}</span>
          <button @click="addToCart(item)">Add to Cart</button>
          <p>{{ item.stock }} in stock</p>
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { defineProps, defineEmits } from 'vue';
  
  const props = defineProps({
    items: Array
  });
  
  const emit = defineEmits(['addToCart']);
  
  function addToCart(item) {
    emit('addToCart', item);
  }
  </script>
  