<template>
  <div class="memory">
    <div 
      class="carte" 
      v-for="(carte, index) in cartes" 
      :key="index" 
      @click="carteRetourner(index)" 
      :class="{ retournee: carte.retournee || carte.trouvee }">
      
      <div class="carte-interieur">
        <div class="face-avant">?</div>
        <div class="face-arriere">
          <img :src="carte.image" alt="image de carte" />
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
import { ref } from 'vue' /* importer la fonction ref de Vue */
import citrouilleImage from '@/assets/pumpkin.png'
import arbreImage from '@/assets/tree.png'
import momieImage from '@/assets/momie.png'
import vampireImage from '@/assets/vampire.png'

// 🔹 Tableau d’images disponibles
const imagesDisponibles = [citrouilleImage, arbreImage, momieImage, vampireImage]

// 🔹 Tirer 2 images aléatoires sans répétition
function tirer2ImagesAleatoires() {

  const imagesChoisies = [] /* tableau vide pour stocker les images choisies */

  // On tire 2 images
  for (let i = 0; i < 2; i++) {
    const indexAleatoire = Math.floor(Math.random() * imagesDisponibles.length) /* on génère un index aléatoire, ente 0 et 4 */
    imagesChoisies.push(imagesDisponibles[indexAleatoire]) /* on ajoute l'image choisie au tableau */
    imagesDisponibles.splice(indexAleatoire, 1) // on retire l'image pour ne pas la reprendre
    console.log(imagesDisponibles) /* on affiche le tableau modifié */
  }

  return imagesChoisies /* on retourne les 2 images choisies */
}

// 🔹 Créer les cartes avec 2 paires
const cartes = ref([])
const imagesPaires = tirer2ImagesAleatoires([])

imagesPaires.forEach(image => {
  cartes.value.push(
    { image, retournee: false, trouvee: false },
    { image, retournee: false, trouvee: false }
  )
})

// 🔹 Mélanger les cartes
cartes.value.sort(() => Math.random() - 0.5)

let cartePremiere = null

function carteRetourner(index) {
  const carte = cartes.value[index]
  if (carte.retournee || carte.trouvee) return

  carte.retournee = true

  if (!cartePremiere) {
    cartePremiere = carte
  } else {
    if (cartePremiere.image === carte.image) {
      cartePremiere.trouvee = true
      carte.trouvee = true
      cartePremiere = null
    } else {
      const cartePrecedente = cartePremiere
      cartePremiere = null
      setTimeout(() => {
        cartePrecedente.retournee = false
        carte.retournee = false
      }, 700)
    }
  }
}
</script>


<style>
.memory {
  display: grid; /* Utilise une grille CSS */
  grid-template-columns: repeat(2, 100px); /* 2 colonnes de 100px */
  gap: 15px;
  justify-content: center;
  margin-top: 70px;
  margin-bottom: -80px;

}
.carte {
  width: 100px;
  height: 120px;
  perspective: 1000px;
}
.carte-interieur {
  position: relative;
  width: 100%;
  height: 100%;
  transition: transform 0.6s;
  transform-style: preserve-3d;
}
.face-avant, .face-arriere {
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2em;
  backface-visibility: hidden;
}
.face-avant {
  background-color: rgb(163, 27, 27);
  color: white;
}
.face-arriere {
  background-color: rgb(42, 36, 128);
  transform: rotateY(180deg);
}
.face-arriere img {
  width: 60px;
  height: 60px;
  object-fit: contain;
}
.retournee .carte-interieur {
  transform: rotateY(180deg);
}
</style>