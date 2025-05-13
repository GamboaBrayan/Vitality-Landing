<template>
<div id="aboutus" class="about gap-20">
    <div class="about-image">
      <img src="../assets/Nosotros.jpg" alt="team vitality">
    </div>
    <div class="container">
      <h2 class="text-3xl mb-4">¿Quiénes somos?</h2>
      <p class="max-w-full">En <strong>Vitality</strong>, creemos que una alimentación saludable es la base para una vida plena y energética. Somos un equipo de nutricionistas, chefs y apasionados por el bienestar, comprometidos a ayudarte a alcanzar tus metas de salud de manera sencilla, deliciosa y sostenible.</p>
      <br>
      <p class="max-w-full">Nuestra misión es transformar la forma en que te relacionas con la comida. No se trata solo de dietas restrictivas o recetas aburridas; en Vitality, te ofrecemos <strong>planes personalizados</strong> y <strong>recetas equilibradas</strong> que se adaptan a tu estilo de vida, gustos y necesidades.</p>
    </div>
</div>
</template>

<style scoped>
.about {
  background-color: #f8f9fa;
  display: flex;
  grid-template-columns: 1fr 1fr; /* Dos columnas de igual tamaño */
  align-items: center; /* Alinea verticalmente los elementos */
  padding: 110px 170px;
  max-width: 100%; /* Ancho máximo del hero */
  margin: 0 auto;
}

.about img {
  max-width: 100%;
  border-radius: 10px;

}

.about p{
 font-size: 17px;
}

@media (max-width: 768px) {
  .about {
    flex-direction: column; /* Apila imagen y texto */
    padding: 60px 20px;
    text-align: center;
  }

  .about img {
    margin-bottom: 30px;
    max-width: 100%; /* Evita que la imagen toque los bordes */
  }

  .about p {
    font-size: 15px;
  }
}

</style>