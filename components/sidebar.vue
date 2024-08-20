<!-- pages/index.vue -->
<template>
    <div>
      <div class="sidebar">
        <nav>
          <ul>
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact</NuxtLink></li>
          </ul>
        </nav>
      </div>
      <div class="main-content">
        <h1>Home Page</h1>
        <p>Welcome to the home page.</p>
      </div>
    </div>
  </template>
  
  <style scoped>
  .sidebar {
    width: 250px;
    height: 100vh;
    background: #333;
    color: #fff;
    position: fixed;
    top: 0;
    left: 0;
    padding: 20px;
  }
  .main-content {
    margin-left: 250px;
    padding: 20px;
  }
  nav ul {
    list-style: none;
    padding: 0;
  }
  nav ul li {
    margin: 10px 0;
  }
  nav ul li a {
    color: #fff;
    text-decoration: none;
  }
  </style>
  