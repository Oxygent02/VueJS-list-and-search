<template>
  <div id="app">
    <navbar-starwars></navbar-starwars>
    <float-button  @character-added="showCharacters"></float-button>
    <character-list :characters="characters"></character-list>
  </div>
</template>

<script>
import navbarStarwars from "./components/navbarStarwars";
import floatButton from "./components/floatButton";
import characterList from "./components/characterList";

export default {
  name: "App",
  components: {
    navbarStarwars,
    floatButton,
    characterList
  },
  data(){
    return{
      characters: []
    }
  },
  methods:{
    showCharacters(payload){
      this.characters = payload;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  position: relative;
}
</style>
