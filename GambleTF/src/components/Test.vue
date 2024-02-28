<template>
    <div class="sidebar">
      <h2>Checkout Cart</h2>
      <div id="cart-items" class="STUFF">
        <div v-for="item in cartItems" :key="item.id" class="cart-item">
          {{ item.name }} <span>${{ item.price.toFixed(2) }}</span>
          <button @click="removeFromCart(item)">Remove</button>
        </div>
      </div>
      <div class="total">
        Total: ${{ total.toFixed(2) }}
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps, defineEmits, computed } from 'vue';
  
  const props = defineProps({
    cartItems: Array
  });
  
  const emit = defineEmits(['removeFromCart']);
  
  function removeFromCart(item) {
    emit('removeFromCart', item);
  }
  
  const total = computed(() => {
    return props.cartItems.reduce((acc, item) => acc + item.price, 0);
  });
  </script>
  
  
  <style scoped>
 
  .STUFF .cart-item {
    list-style-type: none;
    width: 150px;
    height: auto; 
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f9f9f9;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    margin-right: 10px; 
  }
  
  #cart-items {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 0;
    margin: 0;
  }
  
  button {
    margin-top: 10px; 
  }


  .sidebar {
    height: 100vh; 
    background-color: #f0f0f0; 
    flex: 0 0 200px; 
    height: 100vh; 
    padding: 20px;
    border: 1px solid #ccc;
    margin-left: 20px; 
  }

  .total {
  margin-top: 20px;
  text-align: right;
  font-size: 18px;
  font-weight: bold;
}

.sidebar {
  height: 100vh; 
  background-color: #f0f0f0;
  flex: 0 0 200px;
  padding: 20px;
  border: 1px solid #ccc;
  margin-left: 20px;
  overflow-y: auto; 
}
  </style>
  


 