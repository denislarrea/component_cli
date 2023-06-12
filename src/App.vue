<template>
  <div>
    <h1 class="main-title">Denis Bike Shop</h1>
    <div class="container">
      <bike-card
        class="card"
        v-for="(bike) in bikes"
        :key="bike.id"
        :titulo="bike.titulo"
        :portada="bike.portada"
        :descripcion="bike.descripcion"
        :precio="bike.precio"
      ></bike-card>
    </div>
  </div>
</template>

<script>
import BikeCard from './components/BikeCard.vue';

export default {
  components: {
    BikeCard,
  },
  data() {
    return {
      bikes: [
        {
          id: 1,
          titulo: 'Etna Pro',
          portada: 'https://venzoargentina.com.ar/wp-content/uploads/2018/01/etna-x-pro-sin-fondo-2-2048x1367.png',
          descripcion: 'Venzo Etna Pro, monocasco de carbono, 1200 grs aprox; Horquilla: Venzo Etna Pro, monocasco de carbono (rígida); Transmisión: Shimano 105 R7000 (22 velocidades)',
          precio: 3200,
        },
        {
          id: 2,
          titulo: 'Etna x Etna',
          portada: 'https://venzoargentina.com.ar/wp-content/uploads/2018/01/etna-sin-fondo.png',
          descripcion: 'Venzo Etna Pro, monocasco de carbono, 1200 grs aprox; Horquilla: Venzo Etna Pro, monocasco de carbono (rígida); Transmisión: Shimano Tiagra 4700 (20 velocidades)',
          precio: 2500,
        },
        {
          id: 3,
          titulo: 'Phoenix 700c',
          portada: 'https://venzoargentina.com.ar/wp-content/uploads/2018/01/phoenix-pro-sin-fondo-2-2048x1367.png',
          descripcion: 'Venzo Phoenix Pro, Aluminio 6061, Horquilla: Venzo Phoenix Pro, Aluminio 6061 (rígida); Transmisión: Shimano Sora R3000 (18 velocidades) / Sensah 16 y 18 velocidades',
          precio: 2000,
        },
        {
          id: 4,
          titulo: 'MTB-X-FORCE',
          portada: 'https://venzoargentina.com.ar/wp-content/uploads/2020/11/x-force-sin-fondo-2048x1367.png',
          descripcion: 'Venzo X-Force monocasco de carbono 1200 grs aprox - NO BOOST; Frenos: Hidraulicos Shimano; Transmisión: Shimano Deore - 12 Velocidades',
          precio: 2000,
        },
        {
          id: 5,
          titulo: 'MTB-EXCEED',
          portada: 'https://venzoargentina.com.ar/wp-content/uploads/2017/12/venzo-exceed-2018.png',
          descripcion: 'Venzo Exceed de aluminio 6061 para eje trasero de 12 mm BOOST - Con suspensión trasera FOX Float 120mm de recorrido; Shimano Deore - 12 velocidades',
          precio: 1500,
        },
      ],
    };
  },
};
</script>

<style scoped>
.main-title {
  text-align: center;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.card {
  width: 18rem;
  margin: 1rem;
}
</style>