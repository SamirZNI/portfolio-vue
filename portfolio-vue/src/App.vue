<template> 
  <div id="app">
    <Header />
    <Memory />
    <Portfolio />
    <Footer />
  </div>
</template>


<script>
import Header from "./components/Header.vue";
import Portfolio from "./components/Portfolio.vue";
import Footer from "./components/Footer.vue";
import Memory from "./components/Memory.vue";


export default {
  components: {
    Portfolio,
    Memory,
    Header,
    Footer,
  },
};
</script>


<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>