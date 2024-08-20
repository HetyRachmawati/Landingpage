
<template>
  <div class="layout">
    <Sidebar />
    <div class="content">
      <Navbar />
      <main class="main-content">
        <Dashboard />
      </main>
    </div>
  </div>
</template>

<script setup>
import Sidebar from '~/components/admin/Sidebar.vue'
import Navbar from '~/components/admin/Navbar.vue'
import Dashboard from '~/components/admin/Dashboard.vue'
</script>

<style scoped>
/* Layout utama */
.layout {
  display: flex;
  height: 100vh;
}

/* Konten utama dengan margin kiri untuk sidebar dan margin atas untuk navbar */
.content {
  margin-left: 250px; /* Lebar sidebar */
  margin-top: 60px; /* Tinggi navbar */
  flex: 1;
}

/* Padding untuk konten utama */
.main-content {
  padding: 2rem;
}
</style>
