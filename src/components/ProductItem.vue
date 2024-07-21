<template>
    <div class="product-item">
      <div v-if="'product1.jpg' == product.image">
        <img src="@/assets/product1.jpg" > 
      </div>
      <div v-if="'product2.jpg' == product.image">
        <img src="@/assets/product2.jpg" > 
      </div>
      <div v-if="'product3.jpg' == product.image">
        <img src="@/assets/product3.jpg" > 
      </div>  
      <div v-if="'product4.jpg' == product.image">
        <img src="@/assets/product4.jpg" > 
      </div>
      <div v-if="'product5.jpg' == product.image">
        <img src="@/assets/product5.jpg" > 
      </div>
      <div v-if="'product6.jpg' == product.image">
        <img src="@/assets/product6.jpg" > 
      </div>                 
      <div class="product-name">
        <p>{{ product.name }}</p>
      </div>
      <div class="product-desc">
        <p>{{ product.desc }}</p>
        <p align="right">
          <button @click="togglePanel">More Details</button>
                <SlideoutPanel :isOpen="isPanelOpen" @toggle="togglePanel">
                   <p align="left">
                      <div v-if="'product1.jpg' == product.image">
                        <img src="@/assets/product1.jpg" > 
                      </div>
                      <div v-if="'product2.jpg' == product.image">
                        <img src="@/assets/product2.jpg" > 
                      </div>
                      <div v-if="'product3.jpg' == product.image">
                        <img src="@/assets/product3.jpg" > 
                      </div>  
                      <div v-if="'product4.jpg' == product.image">
                        <img src="@/assets/product4.jpg" > 
                      </div>
                      <div v-if="'product5.jpg' == product.image">
                        <img src="@/assets/product5.jpg" > 
                      </div>
                      <div v-if="'product6.jpg' == product.image">
                        <img src="@/assets/product6.jpg" > 
                      </div> 
                    {{ product.desc }}
                </p>
                </SlideoutPanel>
              </p>
      </div>

      <!-- <p>${{ product.price }}</p> -->
    </div>
  </template>
  
  <script>
  import SlideoutPanel from './SlideoutPanel.vue';

  export default {
    name: 'ProductItem',
    props: {
      product: Object
    },
    components: {
      SlideoutPanel
    },
    data() {
      return {
        isPanelOpen: false
      };
    },
    methods: {
      togglePanel() {
        this.isPanelOpen = !this.isPanelOpen;
      }
    }  
  }
  </script>
  
  <style>
  .product-item {
    background-color: white;
                padding: 1em;
                margin-bottom: 2em;
                box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
                display: flex;
                width: 90%;
                align-items: center;
                justify-content: left;
  }
  .product-item img {
    padding: 1em;
    width: 150px;
    height: 150px;

  }
  .product-name p {
    padding: 2em;
    width: 50px;
    height: auto;
  }  
  .product-desc p {
    padding: 2em;
    width: 300px;
    height: auto;
  }

  .product-item p {
    padding: 2em;
    width: 300px;
    height: auto;
  }  

  .right-alignn p {
    padding: 2em;
    width: 300px;
    height: auto;
  } 

  
  </style>
  