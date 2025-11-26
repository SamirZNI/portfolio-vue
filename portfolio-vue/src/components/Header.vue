<template>
  <div class="header">
    <section id="banner">
    <img src="@/assets/test.png" id="pp3" alt="Photo de profil" />
        <section id="topPresentation">
          <h1>Samir Ziani</h1>
          <p id="p1">
            Étudiant en BTS SIO (Services Informatiques aux Organisations)
          </p>
        </section>
    </section>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style>
header {
    padding: 8px 0; /* Ajoute de l'espace autour du texte */
}
#banner {
    display: flex;
    height: 100vh; /* Hauteur de la bannière */
    align-items: center; /* Centre verticalement le contenu */
    justify-content: center; /* Centre horizontalement le contenu */
    width: 100%;
}
#pp3 {
    border-radius: 3%;
    width: 25%; 
    margin: 42px; /* Espace autour de l'image */
    opacity: 0;                  /* commence invisible */
    animation: fadeIn 1s forwards; /* animation de fondu en entrée */
}
@keyframes fadeIn { /* définition de l'animation */ 
    to {
        opacity: 1; /* termine complètement visible */
    }
}
#topPresentation {
    display: flex;
    flex-direction: column;
    background-color: #1b1055;
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.459);
    justify-content: center;
    padding: 60px;
    margin-right: 20px;
    margin-top: 20px;
    width: 65%;
    opacity: 0;                  /* commence invisible */
    animation: fadeIn 1.5s forwards; /* animation de fondu en entrée */
}
#topPresentation h1 {
    color: #e2e7ff;
    font-size: 75px;
    text-align: center;
    justify-content: top;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* Ombre pour améliorer la lisibilité */
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bold;
}
#topPresentation #p1 {
    color: #d0d8ff;
    text-align: center;
    font-size: 40px;
    background-color: #251968;
    margin: 65px;
    padding: 10px;
    border-radius: 8px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}
#topPresentation #p2 {
    color: #e2e7ff;
    text-align: center;
    font-size: 32px;
    text-transform: none;
    font-family: 'Times New Roman', Times, serif;
    padding-top: 50px;
}
#separateur { /*ligne de séparation blanche avec la page principal et les autres*/
    height: 4px;
    width: 70%;
    margin: 0 auto; /* Centrer horizontalement */
    justify-content: center;
    background: linear-gradient(to right, rgba(0,0,0,0), rgb(199, 198, 255), rgba(255, 255, 255, 0));
}
</style>