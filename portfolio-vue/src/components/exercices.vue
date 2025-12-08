<template>
  <div>
    <h2>Liste :</h2>
    <ul>
      <li v-for="mot in liste" :key="mot">
        {{ mot }}
      </li>
    </ul>

    <input v-model="element" type="text" />

    <button @click="danstab">Ajouter à la liste</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      element: "",
      liste: [],
    };
  },

  methods: {
    danstab() {
      if (this.element !== "") {
        this.liste.push(this.element);
        this.element = "";
      }
    },
  },
};
</script>

<style scoped></style>
