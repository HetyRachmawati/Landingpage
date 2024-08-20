<template>
    <header class="navbar">
      <div class="navbar-content">
        <div class="profile-menu">
          <button class="profile-button">Profile</button>
          <div class="dropdown-content">
            <nuxt-link to="/settings">Settings</nuxt-link>
            <nuxt-link to="/logout">Logout</nuxt-link>
          </div>
        </div>
      </div>
    </header>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  /* Navbar styling */
  .navbar {
    background-color: #fff; /* Warna latar belakang putih */
    color: black; /* Warna teks */
    padding: 1rem;
    display: flex;
    justify-content: flex-end; /* Menyusun item di sebelah kanan */
    align-items: center;
    position: fixed;
    top: 0;
    left: 250px; /* Menyesuaikan dengan lebar sidebar */
    right: 0;
    border-bottom: 2px solid #ddd; /* Garis bawah navbar */
    z-index: 10; /* Navbar di bawah sidebar */
  }
  
  /* Konten di dalam navbar */
  .navbar-content {
    display: flex;
    align-items: center;
  }
  
  /* Menu profil */
  .profile-menu {
    position: relative;
  }
  
  /* Tombol profil */
  .profile-button {
    background-color: #f0f0f0; /* Latar belakang terang */
    color: black;
    border: 1px solid #ddd; /* Border tombol */
    padding: 0.5rem 1rem;
    cursor: pointer;
    border-radius: 4px;
    margin-right: 2rem;
  }
  
  /* Hover effect pada tombol profil */
  .profile-button:hover {
    background-color: #e0e0e0; /* Latar belakang sedikit lebih gelap */
  }
  
  /* Dropdown menu di bawah tombol profil */
  .dropdown-content {
    display: none;
    position: absolute;
    top: 100%;
    right: 0;
    background-color: white;
    color: black;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
    z-index: 1;
  }
  
  /* Style untuk link dalam dropdown */
  .dropdown-content a {
    color: black;
    padding: 1rem;
    text-decoration: none;
    display: block;
  }
  
  /* Hover effect pada link dropdown */
  .dropdown-content a:hover {
    background-color: #f1f1f1;
  }
  
  /* Menampilkan dropdown saat hover pada menu profil */
  .profile-menu:hover .dropdown-content {
    display: block;
  }
  </style>
  