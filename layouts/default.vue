<template>
    <div class="layout">
      <Sidebar />
      <div class="content">
        <Navbar />
        <main class="main-content">
          <slot />
        </main>
      </div>
    </div>
  </template>
  
  <script setup>
  import Sidebar from '~/components/admin/Sidebar.vue'
  import Navbar from '~/components/admin/Navbar.vue'
  </script>
  
  <style scoped>
  .layout {
    display: flex;
    height: 100vh;
    overflow: hidden; /* Prevent scroll bars on the outer container */
  }
  
  .content {
    margin-left: 250px; /* Width of the Sidebar */
    margin-top: 60px; /* Height of the Navbar */
    flex: 1;
    overflow: auto; /* Allows the content area to scroll */
  }
  
  .main-content {
    padding: 2rem;
  }
  </style>
  