<template>
    <div class="container">
      <h2><span>Ophams</span> Catalogue</h2>
      <div class="products">
        <div v-for="product in products" :key="product.id" class="product-card">
          <img :src="product.image" class="product-image" alt="Product Image">
          <div class="product-details">
            <h5 class="product-title">{{ product.name }}</h5>
            <p class="product-category">{{ product.category }}</p>
            <p class="product-price">{{ product.price }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const products = [
    {
      id: 1,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju1.png', // Ganti dengan path gambar yang sesuai
    },
    {
      id: 2,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju2.png',
    },

    {
      id: 3,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju3.png',
    },

    {
      id: 4,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju4.png',
    },

    {
      id: 5,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju5.png',
    },
    {
      id: 6,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju1.png',
    },
    {
      id: 7,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju2.png',
    },
    {
      id: 8,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju3.png',
    },
    {
      id: 9,
      name: 'T-shirt',
      category: 'Outfit Boyfriend',
      price: 'Rp. 150.000',
      image: '/img/baju4.png',
    },

    // Tambahkan produk lainnya
  ]
  </script>
  
  <style scoped>
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;

  }

  h2 {
    text-align: center;
    margin-bottom: 40px;
    font-size: 3rem;
    font-weight: bold;
  }

  .container h2 span {
    color: #757575;
  }
  
  .products {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  
  .product-card {
    width: 23%;
    margin-bottom: 20px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    overflow: hidden;
    text-align: center;
    transition: transform 0.3s;
  }
  
  .product-card:hover {
    transform: scale(1.05);
  }
  
  .product-image {
    width: 100%;
    height: auto;
  }
  
  .product-details {
    padding: 10px;
  }
  
  .product-title {
    font-size: 1.2em;
    margin: 10px 0;
  }
  
  .product-category {
    color: #757575;
    margin-bottom: 10px;
  }
  
  .product-price {
    color: #d32f2f;
    font-weight: bold;
  }
  </style>
  