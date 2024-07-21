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

        { id: 1, name: 'Mobile Phones', price: 29.99, image: 'product4.jpg', desc: 'New Cellphones now available for Employees'},
        { id: 2, name: 'New Car Purchases', price: 59.99, image: 'product5.jpg', desc: 'Get 20% off on new car purchases'},
        { id: 3, name: 'Internet Providers', price: 19.99, image: 'product6.jpg', desc: 'Get great deals on internet service'},
        { id: 4, name: 'Toyota Deals', price: 59.99, image: 'product5.jpg', desc: 'Get coupons on services'},

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
  