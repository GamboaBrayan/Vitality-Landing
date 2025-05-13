<template>
<div id="benefits" class="benefits">
    <div class="container">
      <h2 class="text-2xl pb-5 font-bold">¿Por qué elegir Vitality?</h2>
      <div class="benefits-grid text-1xl">
        <div class="benefit flex flex-col items-center">
          <img src="../assets/natural.png" alt="Imagen algo natural">
          <h3 class="font-bold">100% Natural</h3>
          <p>Productos sin aditivos ni conservantes artificiales.</p>
        </div>
        <div class="benefit flex flex-col items-center">
          <img src="../assets/energy.png" alt="imagen de energía">
          <h3 class="font-bold">Energía para todo el día</h3>
          <p>Alimentos ricos en nutrientes que te mantienen activo.</p>
        </div>
        <div class="benefit flex flex-col items-center">
          <img src="../assets/health.png" alt="imagen de salud">
          <h3 class="font-bold">Salud garantizada</h3>
          <p>Certificados por expertos en nutrición.</p>
        </div>
      </div>
    </div>
</div>

</template>

<style scoped>
.benefits {
  background: #f8f9fa;
  padding: 50px 0;
  text-align: center;
}

.benefits-grid {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding-bottom: 20px;

}

.benefit {
  flex: 1 1 30%;
  margin: 10px;
}

.benefit img {
  justify-content: center;
  max-width: 105px;
}

.benefit h3 {
  font-size: 19px;
  margin: 10px 0;
}
.benefit p{
    font-size: 16px;
}

@media (max-width: 768px) {
  .benefits-grid {
    flex-direction: column;
  }
  .benefit {
    flex: 1 1 100%;
    margin: 15px 0;
  }
}
</style>