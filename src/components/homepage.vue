<template>
    <div class="bank-homepage">
      <header class="bank-header">
        <h1>Welcome to MyBank</h1>
      </header>
      <nav class="bank-nav">
        <ul>
          <li><router-link to="/skull">Skull</router-link></li>
          <li><router-link to="/accounts">Accounts</router-link></li>
        </ul>
      </nav>
      <router-view></router-view>
      <footer class="bank-footer">
        <p>&copy; 2023 MyBank</p>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'BankHomepage',
  }
  </script>
  
  <style scoped>
  .bank-homepage {
    background-color: #0074e4;
    color: #ffffff;
    font-family: Arial, sans-serif;
    text-align: center;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .bank-header {
    padding: 20px;
  }
  
  .bank-nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
  }
  
  .bank-nav li {
    margin: 10px;
  }
  
  .bank-nav a {
    text-decoration: none;
    color: #ffffff;
    font-weight: bold;
    font-size: 18px;
  }
  
  .bank-footer {
    padding: 10px;
    background-color: #0050a7;
  }
  </style>
  