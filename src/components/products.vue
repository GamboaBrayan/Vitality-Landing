<script>
// Importa Glide.js
import Glide from '@glidejs/glide';
import '@glidejs/glide/dist/css/glide.core.min.css';

export default {
  data() {
    return {
      products: [
        {
          name: "Batido Energético",
          description: "Lleno de vitaminas y minerales.",
          price: "$10.00",
          image: "/images/batido.jpg",
          nutrition: "Ingredientes: Plátano, espinaca, almendras, leche de coco.",
          calorias: "Calorías: 250 kcal.",
          isFlipped: false,
        },
        {
          name: "Ensalada Vital",
          description: "Fresca y lista para comer.",
          price: "$8.00",
          image: "/images/ensalada.jpg",
          nutrition: "Ingredientes: Lechuga, tomate, aguacate, pollo a la parrilla.",
          calorias: "Calorías: 300 kcal.",
          isFlipped: false,
        },
        {
          name: "Snacks Saludables",
          description: "Perfectos para cualquier momento.",
          price: "$5.00",
          image: "/images/snacks.jpeg",
          nutrition: "Ingredientes: Nueces, almendras, pasas, arándanos.",
          calorias: "Calorías: 200 kcal.",
          isFlipped: false,
        },
        {
          name: "Jugo Detox",
          description: "Desintoxica y revitaliza.",
          price: "$5.00",
          image: "/images/detox.jpg",
          nutrition: "Ingredientes: Pepino, apio, manzana, jengibre.",
          calorias: "Calorías: 150 kcal.",
          isFlipped: false,
        },
        {
          name: "Bowl de Açaí",
          description: "Energía y sabor en cada cucharada.",
          price: "$5.00",
          image: "/images/bowl.jpg",
          nutrition: "Ingredientes: Açaí, plátano, granola, frutas frescas.",
          calorias: "Calorías: 280 kcal.",
          isFlipped: false,
        },
        {
          name: "Smoothie de Frutos Rojos",
          description: "Delicioso y lleno de antioxidantes.",
          price: "$5.00",
          image: "/images/frutosrojos.jpg",
          nutrition: "Ingredientes: Fresas, arándanos, frambuesas, yogur natural. ",
          calorias : "Calorías: 180 kcal",
          isFlipped: false,
        },
      ],
    };
  },
  methods: {
    // Voltear la tarjeta
    flipCard(index) {
      this.products[index].isFlipped = !this.products[index].isFlipped;
    },
  },
  mounted() {
    // Inicializa Glide.js
    new Glide('.glide', {
      type: 'carousel',
      perView: 3, // Muestra 3 tarjetas a la vez
      gap: 30,
    }).mount();
  },
};
</script>


<template>
  <div id="productos" class="productos">
    <div class="container">
      <h2>Nuestros productos estrella</h2>
      <div class="products-carousel">
        <!-- Carrusel de Glide -->
        <div class="glide">
          <div class="glide__track" data-glide-el="track">
            <div class="glide__slides">
              <!-- Slides -->
              <div class="glide__slide" v-for="(product, index) in products" :key="index">
                <div class="product-card" :class="{ flipped: product.isFlipped }" @click="flipCard(index)">
                  <!-- Frente de la tarjeta -->
                  <div class="product-front">
                    <img :src="product.image" :alt="product.name" />
                    <h3>{{ product.name }}</h3>
                    <p>{{ product.description }}</p>
                    <p class="price">{{ product.price }}</p>
                    <button class="btn_ver-mas">Ver más</button>
                  </div>
                  <!-- Parte trasera de la tarjeta -->
                  <div class="product-back">
                    <h3 class="text-xl">Información Nutricional</h3>
                    <p>{{ product.nutrition }}</p>
                    <p>{{ product.calorias }}</p>
                    <button class="btn_volver">Volver</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- Flechas de navegación -->
          <div class="glide__arrows" data-glide-el="controls">
            <button class="carousel-btn glide__arrow glide__arrow--left" data-glide-dir="<">&#10094;</button>
            <button class="carousel-btn glide__arrow glide__arrow--right" data-glide-dir=">">&#10095;</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.products-carousel {
  position: relative;
  padding-bottom: 5%;
}

.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  color: rgb(0, 0, 0);
  border: none;
  padding: 10px;
  cursor: pointer;
  z-index: 10;
}

.glide__arrow--left {
  left: -45px;
}

.glide__arrow--right {
  right: -45px;
}

/* Estilos para las tarjetas */
.product-card {
  margin-bottom: 50px;
  margin-top: 50px;
  position: relative;
  width: 100%;
  height: 400px;
  perspective: 1000px;
  cursor: pointer;
}

.product-front,
.product-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  transition: transform 0.6s ease;
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: 20px;
  box-sizing: border-box;
  background-color: #fff;
}

.product-back {
  transform: rotateY(180deg);
}

.product-card.flipped .product-front {
  transform: rotateY(180deg);
}

.product-card.flipped .product-back {
  transform: rotateY(0deg);
}

/* Estilos para las imágenes y texto */
img {
  object-fit: cover;
  width: 100%;
  height: 200px; 
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  border-radius: 10px;
}

h3 {
  margin: 10px 0;
  font-weight: bold;  
}

p {
  margin: 5px 0;
}
h2{
  font-size: 35px;
  color: white;
  text-align: center;
  padding: 35px;
}
.price {
  font-weight: bold;
  color: #070707;
}

.btn_ver-mas {
  margin-top: 10px;
  padding: 10px 20px;
  background-color: #34db34;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn_volver{
  margin-top: 180px;
  padding: 10px 20px;
  background-color: #34db34;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn:hover {
  background-color: #46b929;
}

@media (max-width: 768px) {
  .carousel-btn {
    display: none !important;
  }

  .product-card {
    height: auto;
    min-height: 280px;
    margin: 20px 0;
  }

  /* 3. Contenedores internos flexibles */
  .product-front,
  .product-back {
    position: relative;
    height: auto;
    min-height: 280px;
    padding: 15px;
  }

  img {
    height: 120px;
    margin-bottom: 10px;
  }

  .btn_ver-mas {
    margin-top: 15px;
  }

  .btn_volver {
    margin-top: 20px; 
    position: static;
  }
}
</style>