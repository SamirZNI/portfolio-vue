<template>
  <div>
    <input v-model="message" type="text" placeholder="Tapez quelque chose">
    <addlist :items="message ? [message] : []" />
    <li v-for="value in source" :key="value">{{ value }}</li>

    <p>Vous avez tapé : {{ message }}</p>
  </div>
</template>

<script>

export default {
  data() {
    return {
      message: ''
    }
  },
}
</script>

<style scoped>

</style>