<template>
    <header class="header">
      <div class="logo">
        <img src="@/assets/image.png" alt="Better Tomorrow Logo">
      </div>
      <div class="search-bar">
        <input type="text" placeholder="Search (Categories, Brands ...)">
        <button>Search</button>
      </div>
      <div class="company-logo">
        <img src="@/assets/CompanyLogo.png" > 
      </div>      
      <div class="user-options">
        <span>Hi, ABC - abc@xyz.com</span>
      </div>

    </header>
    <nav class="nav-bar">
            <a href="/about" id="new">New & Featured</a>
            <a href="/popular" id="popular">Popular Perks</a>
            <a href="#">Health</a>
            <a href="#">More</a>
        </nav>   
  </template>
  
  <script>
  export default {
    name: 'Header',
    methods: {
      new() {  
        alert('yup')
      }
    }
  }

  </script>
  
  <style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    background-color: #1d4d8b;
    color: white;
  }
  .logo img {
    height: 90px;
  }
  .search-bar {
    display: flex;
  }
  .search-bar input {
    width: 400px;
    padding: 5px;
  }
  .search-bar button {
    padding: 5px 10px;
    background-color: #de683e83;
    border: none;
    cursor: pointer;
  }
  .user-options span {
    margin: 0 10px;
    cursor: pointer;
  }
  .company-logo img {
    padding: 1em;
    width: 100px;
    height: 100px;

  }
  
  </style>
  