<template>
  <nav class="navbar">
    <div class="container">
      <router-link to="/" class="logo">Logo</router-link>
      <ul class="nav-links">
        <li><router-link to="/" class="nav-link" exact>Home</router-link></li>
        <li><router-link to="/about" class="nav-link">About</router-link></li>
        <li><router-link to="/services" class="nav-link">Services</router-link></li>
        <li><router-link to="/contact" class="nav-link">Contact</router-link></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>
/* Navbar styles */
.navbar {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 24px;
    color: #fff;
    text-decoration: none;
}

.nav-links {
    list-style: none;
    display: flex;
}

.nav-links li {
    margin-right: 20px;
}

.nav-links li a {
    color: #fff;
    text-decoration: none;
}

.nav-links li a.active {
    font-weight: bold;
}
</style>
