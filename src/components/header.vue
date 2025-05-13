<script setup>

</script>

<template>
  <div id="nav" class="nav">
    <div class="container bg-rgba-white">
      <div class="logo">
        <img src="../assets/VITALITY.png" alt="Logo">
      </div>
      <ul class="nav-links">
        <li><a href="#hero">Inicio</a></li>
        <li><a href="#aboutus">Nosotros</a></li>
        <li><a href="#productos">Productos</a></li>
        <li><a href="#testimonial">Testimonios</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </div>
  </div>
  
</template>

<style scoped>
.nav {
  max-width: 100%;
  background: rgba(255, 255, 255, 0.9); /* Fondo semi-transparente */
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1000;
}

.nav .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
}

.nav .logo img {
  height: 35px;
}

.nav .nav-links {
  list-style: none;
  display: flex;
  gap: 20px;
  margin: 0;
  padding: 0;
}

.nav .nav-links a {
  text-decoration: none;
  color: #333;
  font-weight: 600;
  transition: color 0.3s;
}

.nav .nav-links a:hover {
  color: #218838;
}

@media (max-width: 768px) {
  .nav {
    padding: auto;
    max-width: 100%;
  }

  .nav .container {
    padding: 10px 20px; 
    max-width: 100%;
  }

  .nav .nav-links {
    display: none;
  }

  .nav .menu-toggle {
    display: block; /* Actívalo si usas un botón para móvil */
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
  }

}

</style>
