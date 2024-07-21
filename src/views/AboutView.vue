<template>
    <div id="homepage">
      <Header />
      <ProductList />
      <Footer />
    </div>
  </template>
  
  <script>
  import Header from '../components/Header.vue';
  import ProductList from '../components/ProductList.vue';
  import Footer from '../components/Footer.vue';
  
  export default {
    name: 'App',
    components: {
      Header,
      ProductList,
      Footer
    }
  }
  </script>
  
  <style>
  @media (min-width: 1024px) {
    .about {
      min-height: 100vh;
      display: flex;
      align-items: center;
    }
    body {
              font-family: Arial, sans-serif;
              margin: 0;
              padding: 0;
              background-color: #f4f4f4;
          }
          .header {
              background-color: #0c3568;
              color: white;
              padding: 1em 0;
              display: flex;
              align-items: center;
              justify-content: space-between;
          }
          .header-logo {
              margin-left: 1em;
          }
          .header-logo img {
              width: 100px;
          }
          .search-bar {
              flex-grow: 2;
              margin: 0 1em;
          }
          .search-bar input {
              width: 100%;
              padding: 0.5em;
              border: none;
          }
          .search-bar button {
              padding: 0.5em;
              border: none;
              background-color: #699bfe;
              cursor: pointer;
          }
          .nav-bar {
              background-color: #37475a;
              color: white;
              padding: 1em;
              display: flex;
              justify-content: flex-start;
          }
          .nav-bar a {
              color: white;
              margin: 0 1em;
              text-decoration: none;
          }
          .container {
              width: 80%;
              margin: 2em auto;
          }
          .product {
              background-color: white;
              padding: 1em;
              margin-bottom: 2em;
              box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
              display: flex;
          }
          .product img {
              width: 150px;
              margin-right: 1em;
          }
          .product-details {
              flex-grow: 1;
          }
          .product-details h2 {
              margin-top: 0;
          }  
  }
  </style>
  