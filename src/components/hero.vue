<template>
<div class="hero" id="hero">
    <div class="hero-content">
      <h1>Bienvenido a Vitality!</h1>
      <p>Transforma tu vida, un bocado a la vez. Descubre recetas deliciosas y planes personalizados que nutren tu cuerpo y energizan tu día.</p>
      <button>Comprar</button>
    </div>
    <div class="hero-image">
      <img src="../assets/hero.jpg" alt="Imagen descriptiva">
    </div>
</div>
</template>

<style scoped>
.hero {
  background-color: white;
  display: grid;
  grid-template-columns: 1fr 1fr; /* Dos columnas de igual tamaño */
  align-items: center;
  gap: 20px; /* Espacio entre el texto y la imagen */
  padding: 165px;
  max-width: 100%;
  margin: 0 auto;
}

.hero-content h1 {
  font-size: 52px;
  margin-bottom: 10px;
}

.hero-content p {
  max-width: 85%;
  font-size: 20px;
  margin-bottom: 20px;
}

.hero-content button {
  margin-top: 84px;
  display: flex;
  padding: 10px 20px;
  font-size: 1rem;
  background-color: #28a745;
  color: rgb(255, 255, 255);
  border: none;
  cursor: pointer;
  border-radius: 7px;
}

.hero-content button:hover{
  color: #218838;
}

.hero-image img {
  max-width: 110%;
  height: auto;
  border-radius: 10px;
}

@media (max-width: 768px) {
  .hero {
    grid-template-columns: 1fr; /* Cambia a una sola columna */
    padding: 60px 20px;
    text-align: center;
  }

  .hero-content h1 {
    font-size: 32px;
  }

  .hero-content p {
    max-width: 100%;
    font-size: 16px;
    margin: 0 auto 20px;
  }

  .hero-content button {
    margin-top: 30px;
    margin-left: auto;
    margin-right: auto;
  }

  .hero-image img {
    max-width: 100%; 
    margin-top: 30px;
  }
}

</style>