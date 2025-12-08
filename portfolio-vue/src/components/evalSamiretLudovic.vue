<template>
  <div id="app">
    <!-- Champ de saisie lié à la variable -->
    <input v-model="nouvelElement" type="text" @keyup.enter="ajouterElement" />

    <!-- Bouton pour ajouter l'élément à la liste -->
    <button @click="ajouterElement">Ajouter</button>

    <!-- Liste des éléments avec bouton de suppression -->
    <ul>
      <li v-for="(item, index) in liste" :key="item">
        {{ item }}
        <button @click="supprimerElement(index)">Supprimer</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Variable pour stocker le nouvel item
      nouvelElement: "",

      // Tableau contenant des éléments de départ
      liste: ["1", "2", "3"],
    };
  },
  methods: {
    // Méthode pour ajouter un nouvel élément à la liste
    ajouterElement() {
      if (this.nouvelElement !== "") {
        this.liste.push(this.nouvelElement); // ajout dans la liste
        this.nouvelElement = ""; // vider le champ après ajout
      }
    },

    // Méthode pour supprimer un élément par son index
    supprimerElement(index) {
      this.liste.splice(index, 1); /* suppression de l'élément, index c'est les elements dans le tableau, "1" c'est le nombre d'element supprimer */
    },
  },
};
</script>
