
<template>
  <div class="layout">
    <Sidebar />
    <div class="content">
      <Navbar />
      <div class="container-fluid">
        <!-- Page Heading -->
        <h1 class="h3 mb-2 text-gray-800">Tables</h1>
        <p class="mb-4">
          DataTables is a third party plugin that is used to generate the demo table below.
          For more information about DataTables, please visit the
        </p>

        <!-- Button to Create Data -->
        <div class="d-flex justify-content-start mb-3">
          <button class="btn btn-primary">Tambahkan Data</button>
        </div>

        <!-- DataTales Example -->
        <div class="card shadow mb-4">
          <div class="card-header py-3 d-flex justify-content-between align-items-center">
            <h6 class="m-0 font-weight-bold text-primary">DataTables Example</h6>
            <!-- Search Input -->
            <div class="search-container">
              <input
                type="text"
                class="form-control"
                placeholder="Search..."
                v-model="searchQuery"
              />
            </div>
          </div>
          <div class="card-body">
            <div class="table-responsive">
              <table class="table table-bordered" id="dataTable" width="100%" cellspacing="0">
                <thead>
                  <tr>
                    <th>Id</th>
                    <th>Nama</th>
                    <th>Aksi</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="item in filteredData" :key="item.name">
                    <td>{{ item.id}}</td>
                    <td>{{ item.nama}}</td>
                    <td>{{ item.aksi }}</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  // Your script code here
</script>

<style scoped>
.container-fluid {
  padding: 2rem;
  margin-top: 60px; /* Space for Navbar */
  margin-left: 15rem;
}

.card {
  border-radius: 0.5rem;
  margin-right: 15rem;
}

.card-header {
  background-color: #f8f9fc;
  position: relative;
}

.search-container {
  position: absolute;
  right: 1rem;
  top: 50%;
  transform: translateY(-50%);
  max-width: 300px;
}

.table {
  margin-top: 1rem;
}

.table th, .table td {
  text-align: center;
}

.btn {
  border-radius: 0.3rem;
}
</style>
