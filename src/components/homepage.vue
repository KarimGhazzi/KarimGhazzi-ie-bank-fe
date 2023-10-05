<template>
    <div>
      <header>
        <h1>Welcome to MyBank</h1>
      </header>
      <nav>
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/accounts">Accounts</router-link></li>
          <li><router-link to="/skull">Skull</router-link></li>
        </ul>
      </nav>
      <router-view></router-view>
      <footer>
        <p>&copy; 2023 MyBank</p>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: 'BankHomepage',
  }
  </script>
  
  <style>
  /* Add your CSS styles here */
  </style>
  