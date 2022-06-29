<template>
  <div class="personajes">
    <img :src="datos.src" :alt="datos.nombre" class="imagen" />
    <p>{{ datos.nombre }}</p>
  </div>
</template>

<script>
export default {
  name: "ComponentePersonajes",
  props: {
    datos: {
      type: Object,
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.personajes {
  display: flex;
}
.imagen {
  border-radius: 50%;
  margin-left: 35%;
  margin-bottom: 20px;
  border: 5px solid rgb(21, 180, 21);
}
</style>
