<template>
<section id="contacto"  class="contact-form">
    <h2>Contactanos</h2>
    <form action="#" method="POST">
      <div class="form-group">
        <label for="name">Nombre:</label>
        <input type="text" id="name" name="name" required>
      </div>
      <div class="form-group">
        <label for="email">Correo electrónico:</label>
        <input type="email" id="email" name="email" required>
      </div>
      <div class="form-group">
        <label for="message">Mensaje:</label>
        <textarea id="message" name="message" rows="5" required></textarea>
      </div>
      <button type="submit">Enviar</button>
    </form>
  </section>
</template>

<style>
button {
  display: inline-block;
  padding: 10px 20px;
  background: #28a745;
  color: #fff;
  text-decoration: none;
  border-radius: 5px;
  transition: background 0.3s;
}

.contact-form {

padding: 50px 20px;
background-color: #ffffff;
text-align: center;
}

.contact-form h2 {
font-size: 2rem;
margin-bottom: 20px;
}

.contact-form form {
max-width: 600px;
margin: 0 auto;
text-align: left;
}

.form-group {
margin-bottom: 20px;
}

.form-group label {
display: block;
font-size: 1rem;  
margin-bottom: 5px;
}

.form-group input,
.form-group textarea {
width: 100%;
padding: 10px;
font-size: 1rem;
border: 1px solid #aca7a7;
border-radius: 5px;
}

.form-group textarea {
resize: vertical;
}

@media (max-width: 768px) {
  .contact-form {
    padding: 30px 15px; /* Menos padding en móvil */
  }

  .contact-form h2 {
    font-size: 1.5rem; /* Título más pequeño */
  }

  .contact-form form {
    padding: 0 10px; /* Padding lateral para inputs */
  }

  button {
    padding: 12px 20px; /* Botón más grande para móvil */
    width: 100%; /* Ocupa todo el ancho */
    font-size: 1.1rem; /* Texto más legible */
  }

  .form-group input,
  .form-group textarea {
    padding: 12px; /* Más espacio interno para touch */
    font-size: 0.95rem; /* Texto ligeramente más pequeño */
  }
}
</style>