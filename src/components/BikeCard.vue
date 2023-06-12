
Aquí tienes la estructura finalizada de tu proyecto Vue CLI:

Crea un nuevo proyecto Vue CLI ejecutando el siguiente comando en tu terminal:
bash
Copy code
vue create nombre-del-proyecto
Reemplaza el contenido del archivo index.html del proyecto Vue CLI recién creado con el siguiente código:
html
Copy code
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Web Components</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css">
  <link rel="stylesheet" href="/dist/css/app.css">
</head>
<body>
  <div id="app"></div>

  <!-- Enlace al archivo JS generado por Vue CLI -->
  <script src="/dist/js/app.js"></script>
</body>
</html>
Crea una nueva carpeta llamada css en la raíz del proyecto Vue CLI y mueve el archivo estilos.css dentro de ella.

Abre el archivo src/main.js y reemplaza todo el contenido con el siguiente código:

javascript
Copy code
import Vue from 'vue';
import App from './App.vue';

Vue.config.productionTip = false;

new Vue({
  render: (h) => h(App),
}).$mount('#app');
Crea una nueva carpeta llamada components dentro de la carpeta src. Luego, crea un nuevo archivo llamado BikeCard.vue dentro de la carpeta components y copia el siguiente código en él:
html
Copy code
<template>
  <div class="card">
    <img :src="portada" class="card-img-top" :title="titulo">
    <div class="card-body">
      <h5 class="card-title">{{ titulo }}</h5>
      <p class="card-text">{{ descripcion }}</p>
      <p class="card-text">Usd<strong> {{ precio }}</strong></p>
      <button class="btn btn-success btn-rounded">Agregar</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    titulo: String,
    portada: String,
    descripcion: String,
    precio: Number,
  },
};
</script>

<style scoped>
/* Agrega los estilos de tu componente de tarjeta de bicicleta */
</style>