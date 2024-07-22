<template>
    <div class="product-list">
      <ProductItem v-for="product in products" :key="product.id" :product="product" />
    </div>
  </template>
  
  <script>
  import ProductItem from './ProductItem.vue';
  
  export default {
    name: 'ProductList',
    components: {
      ProductItem
    },
    data() {
      return {
        products: [
          { id: 1, name: 'Adidas', price: 29.99, image: 'product1.jpg', desc: 'Adidas is a leading sports shoes and apparel provider.'},
          { id: 2, name: 'Abc International', price: 59.99, image: 'product2.jpg', desc: 'Abc is offering Up to 50% Off New Markdowns + Earn 5% Reward Points'},
          { id: 3, name: 'Wonder Parks', price: 19.99, image: 'product3.jpg', desc: 'Wonder parks is providing a 10% discount for all employees'}
        ]
      };
    }
  }
  </script>
  
  <style>
  .product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 20px;
  }
  </style>
  