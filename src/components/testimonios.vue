<template>
    <section id="testimonial" class="testimonials">
    <div class="container">
      <h2 class="text-3xl pb-5">Lo que dicen nuestros clientes</h2>
      <div class="testimonials-grid">
        <div class="testimonial">
          <img src="../assets/mujer.jpg" alt="Testimonio1">
          <h4>María González</h4>
          <p>"Los productos de Vitalidad cambiaron mi forma de alimentarme. ¡Me siento con más energía que nunca!"</p>
        </div>
        <div class="testimonial">
          <img src="../assets/hombre.jpg" alt="Testimonio2">
          <h4>Carlos López</h4>
          <p>"La mejor decisión para mi salud. ¡Totalmente recomendado!"</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.testimonials {
  background: #f8f9fa;
  padding: 50px 0;
  text-align: center;
}

.testimonials-grid {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.testimonial {
  flex: 1 1 45%;
  margin: 10px;
  background: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.testimonial img {
  max-width: 100px;
  border-radius: 50%;
  margin-bottom: 10px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

</style>