<template> 
  <div id="app">
    <Exercices />
    <!--Header />
    <Memory />
    <Portfolio />
    <Footer /> -->
  </div>
  <!-- <button @click="memory">
    Memory
  </button> -->
</template>


<script>
/* import Header from "./components/Header.vue";
import Portfolio from "./components/Portfolio.vue";
import Footer from "./components/Footer.vue";
import Memory from "./components/Memory.vue"; */
import Exercices from './components/exercices.vue';


export default {
  components: {
    /* Portfolio,
    Memory,
    Header,
    Footer, */
    Exercices,
  },
};
</script>


<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>