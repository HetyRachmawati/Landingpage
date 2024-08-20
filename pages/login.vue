<template>
    <div class="container">
      <div class="image-container">
        <img src="/img/imglogin.png" alt="Ophams Image">
      </div>
      <div class="login-container">
        <div class="login-content">
          <h2>Ophams</h2>
          <form class="login-form">
            <div class="form-group">
              <label for="email">Email</label>
              <input type="email" id="email" name="email" placeholder="Enter Email Here" required>
            </div>
            <div class="form-group">
              <label for="password">Password</label>
              <input type="password" id="password" name="password" placeholder="Enter Password Here" required>
            </div>
            <button type="submit">Login</button>
          </form>
          <p class="terms">
            By signing up, you agree to our <a href="#">Terms & Conditions</a> and <a href="#">Privacy Policy</a>.
          </p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  // Anda dapat menambahkan logika terkait script di sini jika diperlukan
  </script>
  
  <style scoped>
  .container {
    display: flex;
    flex-direction: row;
    min-height: 50vh;
    background-color: white;
  }
  
  .image-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f5f5f5;
  }
  
  .image-container img {
     width: 100%;
  height: 100%;
  object-fit: cover;
  }
  
  .login-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .login-content {
    width: 100%;
    max-width: 400px;
    padding: 20px;
    background-color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 15px;
    text-align: center;
  }
  
  .login-content h2 {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 20px;
  }
  
  .login-form .form-group {
    margin-bottom: 15px;
  }
  
  .login-form label {
    display: block;
    font-size: 14px;
    margin-bottom: 5px;
    text-align: left;
  }
  
  .login-form input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  .login-form button {
    width: 100%;
    padding: 10px;
    background-color: black;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
  }
  
  .login-form button:hover {
    background-color: #333;
  }
  
  .terms {
    margin-top: 15px;
    font-size: 12px;
    color: #666;
  }
  
  .terms a {
    color: #000;
    text-decoration: none;
    font-weight: bold;
  }
  
  .terms a:hover {
    text-decoration: underline;
  }
  </style>
  