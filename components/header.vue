<template>
  <div>

    <!-- Header Section -->
    <header :class="['header', { scrolled }]">
    <div class="logo">Ophams</div>
    <nav class="nav-links">
      <NuxtLink to="#home">Home</NuxtLink>
      <NuxtLink to="#about">About</NuxtLink>
      <NuxtLink to="#collection">Our Collection</NuxtLink>
    </nav>
    <NuxtLink to="/catalog">
      <button class="shop-now">Shop Now</button>
    </NuxtLink>
  </header>

<!-- Hero Section -->
<section class="hero" id="home">
  <div class="hero-content">
    <div class="text-content">
      <h1>DISCOVER <span>OUR</span></h1>
      <h1>TRENDY <span>AND</span></h1>
      <h1>FRESH <span>COLLECTION</span></h1>
      <div class="buttons">
        <button class="get-started">Get Started</button>
        <button class="explore-now">Explore Now</button>
      </div>
    </div>
  </div>
</section>

    <!-- Collection Section -->
    <section class="collection-section">
    <div class="collection-container">
      <h2 class="collection-title">Our New Collection</h2>
      <div class="product-grid">
        <div v-for="item in baju" :key="item.id" class="product-card">
          <img :src="item.gambar" :alt="item.nama" class="product-image" />
          <h3 class="product-name">{{ item.nama }}</h3>
          <p class="product-description">{{ item.deskripsi }}</p>
          <p class="product-price">{{ formatCurrency(item.harga) }}</p>
          <button class="shop-now-button" @click="addToCart(item)">Add to Cart</button>
        </div>
      </div>
      <button class="view-more-button" @click="viewMore">View More</button>
    </div>
  </section>

    <!-- Grid Image -->
    <section id="grid" class="grid">
      <h2>Discover our <span>durable</span> and</h2>
      <h2><span>resilient </span>clothing materials</h2>
      <div class="column">
        <div class="image-grid">
          <div class="image-item1">
            <img src="/img/gambar3.png" alt="Image 1" />
          </div>
          <div class="image-item2">
            <img src="/img/gambar4.png" alt="Image 2" />
          </div>
          <div class="image-item3">
            <img src="/img/gambar5.png" alt="Image 3" />
          </div>
        </div>
      </div>
    </section>

    <!-- About Us-->
    <section class="about-us">
    <div class="text-content">
      <h2>About Us</h2>
      <p>
        At Ophams, we believe that fashion is more than just clothing—it's a way to express your unique personality and style. 
        Ophams has become a premier destination for fashion enthusiasts who crave something distinct and exceptional.
      </p>
    </div>
    <div class="image-content">
      <img src="/img/about.png" alt="About Us Image" />
    </div>
  </section>


    <!-- Newsletter Subscribe Section Get In Tounch-->
    <div class="newsletter-subscribe">
      <div class="left-section">
        <h1>Get In Touch</h1>
        <p>Subscribe to our newsletter</p>
        <p>to get updates of our collections</p>
      </div>
      <div class="right-section">
        <form @submit.prevent="subscribe">
          <input type="email" v-model="email" placeholder="Enter your email here" />
          <button type="submit">subscribe</button>
        </form>
      </div>
    </div>
  </div>
</template>


<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

// Data for products
const baju = ref([
  {
    id: 1,
    nama: "Baju Casual",
    gambar: "/img/baju1.png",
    deskripsi: "Baju casual yang nyaman untuk sehari-hari.",
    harga: 150000
  },
  {
    id: 2,
    nama: "Baju Formal",
    gambar: "/img/baju2.png",
    deskripsi: "Baju formal untuk acara khusus.",
    harga: 250000
  },
  {
    id: 3,
    nama: "Baju Formal",
    gambar: "/img/baju3.png",
    deskripsi: "Baju formal untuk acara khusus.",
    harga: 250000
  },
  {
    id: 4,
    nama: "Baju Formal",
    gambar: "/img/baju4.png",
    deskripsi: "Baju formal untuk acara khusus.",
    harga: 250000
  },

]);

// State for scroll detection
const scrolled = ref(false);

const handleScroll = () => {
  scrolled.value = window.scrollY > 50;
};

// Lifecycle hooks
onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

// Methods
const addToCart = (item) => {
  // Logic for adding product to cart
  console.log('Add to Cart:', item);
};

const viewMore = () => {
  // Logic for viewing more products or navigation
  console.log('View More clicked');
};

// Method to format currency as Rupiah
const formatCurrency = (value) => {
  return `Rp ${value.toLocaleString('id-ID')}`;
};
</script>
