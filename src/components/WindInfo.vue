<template>
  <div class="wind-info">
    <p class="label">Wind</p>
    <div class="wind-value">
      <p>{{ weatherData.current.wind_kph }} km/h</p>
      <p class="wind-direction">{{ weatherData.current.wind_dir }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    weatherData: {
      type: Object,
      required: true
    }
  }
};
</script>

<style scoped>
.wind-info {
 margin: 20px;
 margin-top: 0;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: -5px -5px 9px rgba(255, 255, 255, 0.45), 5px 5px 9px rgba(94, 104, 121, 0.3);
  width: 200px; /* Establecer un ancho específico */
  height: 200px; /* Establecer una altura específica */
  display: flex; /* Establecer el contenedor como flexbox */
   flex-direction: column; /* Establecer la dirección del flujo en columna */
  justify-content: center; /* Centrar horizontalmente el contenido */
  align-items: center; /* Centrar verticalmente el contenido */
}

.wind-info .label {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 10px;
}

.wind-value {
  display: flex;
  flex-direction: column;
  margin-left: 10px;
}

.wind-direction {
  font-size: 18px;
  font-weight: bold;
}
</style>
