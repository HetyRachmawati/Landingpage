<template>
    <aside class="sidebar">
      <h2>Ophams</h2>
      <ul>
        <li><nuxt-link to="/">Dashboard</nuxt-link></li>
        <li><nuxt-link to="/admin/baju">Data Baju</nuxt-link></li>
        <li><nuxt-link to="/logout">Data Jenis Baju</nuxt-link></li>
      </ul>
    </aside>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  /* Sidebar styling */
  .sidebar {
    height: 100vh;
    width: 250px;
    background-color: #333; /* Warna latar belakang sidebar */
    color: white; /* Warna teks */
    padding: 1rem;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    z-index: 20; /* Sidebar di atas elemen lain */
  }
  
  /* Styling untuk judul sidebar */
  .sidebar h2 {
    margin-bottom: 1rem;
    padding-bottom: 0.5rem; /* Jarak antara teks dan garis */
    font-style: italic;
  }
  
  /* Menghilangkan bullet pada list */
  .sidebar ul {
    list-style: none;
    padding: 0;
    font-size: 1.5rem;
  }
  
  /* Margin bawah untuk setiap item list */
  .sidebar ul li {
    margin-bottom: 1rem;
  }
  
/* Styling untuk link dalam list */
.sidebar ul li a {
  color: white; /* Warna teks link */
  text-decoration: none; /* Menghilangkan garis bawah default */
  font-style: initial; /* Mengikuti gaya font dari elemen induk */
}
  /* Hover effect pada link */
  .sidebar ul li a:hover {
    text-decoration: underline; /* Garis bawah saat hover */
  }
  </style>
  