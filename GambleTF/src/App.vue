

<template>
    <div class="container">
      <Items :items="ITEMS" @addToCart="handleAddToCart" />
      <Test :cartItems="cartItems" @removeFromCart="handleRemoveFromCart" />
    </div>
  </template>
  
  <script setup>
  import Test from './components/Test.vue';
  import Items from './components/Items.vue';
  import { ref } from 'vue';
  
  const ITEMS = ref([
    { id: 1, name: 'T-Shirt', price: 19.99 },
    { id: 2, name: 'Jeans', price: 49.99 },
    { id: 3, name: 'Sneakers', price: 89.99 },
    { id: 4, name: 'Hat', price: 12.99 },
    { id: 5, name: 'Sunglasses', price: 15.99 },
    { id: 6, name: 'Backpack', price: 59.99 },
    { id: 7, name: 'Watch', price: 199.99 },
    { id: 8, name: 'Belt', price: 29.99 },
    { id: 9, name: 'Water Bottle', price: 9.99 },
    { id: 10, name: 'Hoodie', price: 39.99 },
    { id: 11, name: 'Scarf', price: 19.99 },
{ id: 12, name: 'Gloves', price: 24.99 },
{ id: 13, name: 'Cap', price: 14.99 },
{ id: 14, name: 'Socks', price: 9.99 },
{ id: 15, name: 'Sweater', price: 59.99 },
{ id: 16, name: 'Jacket', price: 99.99 },
{ id: 17, name: 'Boots', price: 79.99 },
{ id: 18, name: 'Sandals', price: 49.99 },
{ id: 19, name: 'Wristband', price: 5.99 },
{ id: 20, name: 'Leggings', price: 39.99 },
{ id: 21, name: 'Shorts', price: 29.99 },
{ id: 22, name: 'Tie', price: 19.99 },
{ id: 23, name: 'Blouse', price: 45.99 },
{ id: 24, name: 'Dress', price: 89.99 },
{ id: 25, name: 'Skirt', price: 49.99 },
{ id: 26, name: 'Swimsuit', price: 39.99 },
{ id: 27, name: 'Towel', price: 25.99 },
{ id: 28, name: 'Beanie', price: 17.99 },
{ id: 29, name: 'Cardigan', price: 55.99 },
{ id: 30, name: 'Suit', price: 199.99 },
{ id: 31, name: 'Vest', price: 59.99 },
{ id: 32, name: 'Pajamas', price: 39.99 },
{ id: 33, name: 'Robe', price: 69.99 },
{ id: 34, name: 'Slippers', price: 29.99 },
{ id: 35, name: 'Umbrella', price: 24.99 },
{ id: 36, name: 'Wallet', price: 49.99 },
{ id: 37, name: 'Purse', price: 59.99 },
{ id: 38, name: 'Laptop Bag', price: 89.99 },
{ id: 39, name: 'Earphones', price: 29.99 },
{ id: 40, name: 'Smartwatch', price: 199.99 },
{ id: 41, name: 'Bracelet', price: 22.99 },
{ id: 42, name: 'Necklace', price: 35.99 },
{ id: 43, name: 'Earrings', price: 14.99 },
{ id: 44, name: 'Ring', price: 99.99 },
{ id: 45, name: 'Baseball Cap', price: 19.99 },
{ id: 46, name: 'Sports Jersey', price: 99.99 },
{ id: 47, name: 'Yoga Mat', price: 29.99 },
{ id: 48, name: 'Gym Bag', price: 59.99 },
{ id: 49, name: 'Sunglass Case', price: 9.99 },
{ id: 50, name: 'Keychain', price: 4.99 }

  ]);
  
  const cartItems = ref([]);
  
  function handleAddToCart(item) {
    cartItems.value.push(item);
   
  }
  
  function handleRemoveFromCart(item) {
    const index = cartItems.value.findIndex((cartItem) => cartItem.id === item.id);
    if (index > -1) {
      cartItems.value.splice(index, 1);
    }
   
  }
  </script>


<style>
.container {
  display: flex;
    justify-content: space-between

}
</style>
  