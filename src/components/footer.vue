<template>
<footer>
<div class="container" id="footer">
    <!-- Columna 1 -->
    <div class="flex flex-col items-start space-y-2">
        <img src="../assets/VITALITY.png" alt="Logo de Vitality" class="logo-footer">
        <p>Transforma tu vida con recetas y dietas saludables.</p>
        <p>Email: info@vitality.com</p>
        <p>Teléfono: +123 456 789</p>
    </div>
    <!-- Columna 2 -->
    <div class="flex flex-col items-start">
        <h3>Enlaces rápidos</h3>
        <ul class="space-y-1">
        <li><a href="#">Inicio</a></li>
        <li><a href="#">Servicios</a></li>
        <li><a href="#">Recetas</a></li>
        <li><a href="#">Planes de dieta</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Contacto</a></li>
    </ul>
    </div>
    <!-- Columna 3 -->
    <div class="flex flex-col items-start">
        <h3>Síguenos</h3>
        <ul class="space-y-1">
        <li><a href="#">Facebook</a></li>
        <li><a href="#">Instagram</a></li>
        <li><a href="#">Twitter</a></li>
        <li><a href="#">YouTube</a></li>
        </ul>
    </div>
    <!-- Columna 4 -->
    <div class="flex flex-col items-start">
        <h3>Legal</h3> 
        <ul class="space-y-1">
        <li><a href="libro-reclamaciones.html">Libro de reclamaciones</a></li>
        <li><img src="../assets/libro.png" alt="Libro de reclamaciones" class="reclamaciones-footer"></li>
        <li><a href="#">Términos y condiciones</a></li>
        <li><a href="#">Política de privacidad</a></li>
        <li><a href="#">Aviso legal</a></li>
        <li><a href="#">Cookies</a></li>
        </ul>   
    </div>

  </div>

    <div>
        <p>© 2025 Vitality. Todos los derechos reservados.</p>
    </div>
</footer>
</template>

<style scoped>
footer {
  background: #333;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}

footer .container{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  align-items: center; /* Alinea verticalmente los elementos */
  gap: 20px;
  max-width: 85%;
  text-align: left;
  padding-bottom: 20px;
}

footer .logo-footer{
  height: 30px;
}

footer .reclamaciones-footer{
  height: 40px;
}

footer li a{
  color: #ffffff;
  font-size: 15px;
  max-width: 15px;
  text-align: left;
  text-decoration: none;
}

footer ul{
  list-style: none; /* Elimina los puntos de lista */
  padding-left: 0; /* Opcional: elimina el padding izquierdo */
}
</style>