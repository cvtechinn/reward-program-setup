<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/image.png" width="200" height="200" />
    </header>

    <div class="login">
      <h2>Login</h2>
      <form @submit.prevent="login">
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div>
          <label for="password">Password:</label>
          <input type="password" id="password" v-model="password" required>
        </div>
        <button type="submit">Login</button>
      </form>
    </div>
  </template>
  
  <script>
import router from '@/router';

  export default {
    data() {
      return {
        email: '',
        password: ''
      }
    },
    methods: {
      login() {
        // Replace with your actual login logic
        if (this.email === 'abc@gmail.com' && this.password === 'a') {
            alert('Login successful!');
            router.push({ path: 'about' })
        } else {
          alert('Invalid email or password.');
        }
      }
    }
  }
  </script>
  
  <style scoped>    
  
  .login {
    /* max-width: 300px; */
    margin: 0 auto;
    padding: 1em;
    background: #f9f9f9;
    border-radius: 5px;
  }
  .login div {
    margin-bottom: 1em;
  }
  .login label {
    margin-bottom: .5em;
    color: #333333;
    display: block;
  }
  .login input {
    border: 1px solid #CCCCCC;
    padding: .5em;
    font-size: 1em;
    width: 100%;
    box-sizing: border-box;
  }
  .login button {
    padding: 0.7em;
    color: #fff;
    background-color: #007BFF;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  .login button:hover {
    background-color: #0056b3;
  }
  .logo {
  display: block;
  margin: 0 auto 1rem;
    }
  </style>
  