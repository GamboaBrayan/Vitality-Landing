<template>
<div id="cta" class="cta">
    <div class="container ">
      <h2 class="font-bold">¿Listo para empezar tu viaje hacia una vida más saludable?</h2>
      <a href="#productos" class="btn">Comprar ahora</a>
    </div>
</div>
</template>

<style scoped>
.cta {
  background: #28a745;
  color: #fff;
  text-align: center;
  padding: 20px 25px;
}

.cta a {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: white;
  color: black;
}

.cta h2 {
  margin-bottom: 20px;
  font-size: 24px;
}

.btn:hover {
  background: #218838;
}

@media (max-width: 768px) {
  .cta {
    padding: 30px 15px;
  }
  .cta h2 {
    font-size: 20px;
  }
}

</style>