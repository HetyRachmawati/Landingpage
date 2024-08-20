<template>
    <footer class="footer">
      <div class="footer-content">
        <div class="footer-brand">
          <h2>Ophams</h2>
          <p>Meet your fashion needs at all times</p>
          <div class="footer-socials">
            <a href="#"><img src="/img/icon-fb.png" alt="Facebook" /></a>
            <a href="#"><img src="/img/icon-ig.png" alt="Instagram" /></a>
            <a href="#"><img src="/img/icon-twitt.png" alt="Twitter" /></a>
          </div>
        </div>
        <div class="footer-links">
          <a href="#">Company</a>
          <a href="#">Platforms</a>
          <a href="#">Legal</a>
          <a href="#">Blog</a>
          <a href="#">Shop</a>
          <a href="#">Terms & Condition</a>
          <a href="#">Careers</a>
          <a href="#">News</a>
        </div>
      </div>
    </footer>
  </template>
  
  <style scoped>
  .footer {
    padding: 2rem;
    border-top: 1px solid #ccc;
    background-color: grey;
  }
  .footer-content {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
  .footer-brand h2 {
    margin: none;
    font-size: 2rem;
    margin-left: 5rem;
    font-style: bold;
  }
  .footer-brand p {
    margin: 0.5rem 0;
    margin-left: 5rem;
    
  
  }
  .footer-socials {
    display: flex;
    gap: 1rem;
    margin-top: 0.5rem;
    margin-left: 5rem;
  }
  .footer-socials img {
    width: 24px;
    height: 24px;
  }
  .footer-links {
    display: grid;
    grid-template-columns: repeat(3, auto);
    gap: 1rem 2rem;
    font-size: 0.875rem;
    margin-right: 8rem;
  }
  .footer-links a {
    color: black;
    text-decoration: none;
  }
  .footer-links a:hover {
    text-decoration: underline;
  }
  </style>
  