<template> 
  <div id="app">
    <Portfolio />
  </div>
</template>


<script>
import Portfolio from "./components/Portfolio.vue";
import Header from "./components/Header.vue";

export default {
  components: {
    Portfolio,
  },
};
</script>


<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>