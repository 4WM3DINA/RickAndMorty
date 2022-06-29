<template>
  <div id="app">
    <h1>Rick And Morty</h1>
    <ComponentePersonajes
      v-for="(character, index) in characters"
      :key="index"
      :datos="character"
    />
  </div>
</template>

<script>
import ComponentePersonajes from "./components/ComponentePersonajes.vue";

export default {
  name: "App",
  components: {
    ComponentePersonajes,
  },
  data() {
    return {
      characters: [
        {
          nombre: "Rick Sanchez",
          src: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          nombre: "Morty Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          nombre: "Summer Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          nombre: "Beth Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          nombre: "Jerry Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
        {
          nombre: "Abadango Cluster Princess",
          src: "https://rickandmortyapi.com/api/character/avatar/6.jpeg",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  background-image: url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png");
  background-size: cover;
  background-repeat: no-repeat;
  border-radius: 2rem;
  border: 20px solid rgb(119, 23, 23);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-weight: bold;
  font-size: 3rem;
  color: #eb8996;
}
</style>
