<template>
  <div class="header">
    <!-- Menu mobile -->
    <input type="checkbox" id="menu-toggle">
    <label for="menu-toggle" id="menu-icon">&#9776;</label>
    <nav>
      <ul>
        <li><a href="#aPropos">À propos</a></li>
        <li><a href="#competences">Compétences & Technologies</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style>
nav {
    list-style: none; /* Supprime les puces */
    display: flex; /* Affiche les éléments en ligne */
    justify-content: center;
    background-color: #1d1152;
    box-shadow: 0 6px 5px rgba(0, 0, 0, 0.575);
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    /* Pour qu’il reste au-dessus du reste du contenu */
    z-index: 1000; /* Valeur élevée pour rester au-dessus */
}
nav ul {
    list-style: none;
    display: flex; 
    justify-content: center;
    align-items: center;
    margin: 0;
    padding: 13px 0;
}
nav li {
    margin: 0 10px;
}
nav a {
    display: inline-block; /* <-- ajoute cette ligne */
    color: rgb(255, 255, 255);
    font-family: 'berlin sans fb demi', sans-serif;
    font-weight: bold;
    text-shadow: #000000 1px 1px 2px;
    font-size: 16px;
    margin: 0 15px; /* Espace entre les liens */
    text-decoration: none; /* Supprime le soulignement */
}
a:hover { /* Effet au survol du menu (passe la souris dessus) */
    text-decoration: none; /* Supprime le soulignement au survol */
    color: #ffffff;
    text-shadow: 1px 1px 2px #000000;
    transform: scale(1.04); /* Agrandit légèrement le lien au survol */
    transition: 0.4s; /* Animation douce */
}
#menu-icon { /*Bouton menu pour mobile*/
    display: none; /* caché sur PC */
    font-size: 29px; /* un peu plus grand pour mobile */
    color: rgb(255, 255, 255);
    padding: 8px;
    background-color: #140568;
    border-radius: 7px;
    box-shadow: #000000 1px 1px 2px;
    position: fixed;
    top: 18px;
    left: 24px;
    z-index: 1100;
    cursor: pointer;
}
#menu-toggle {
    display: none;
}

@media (max-width: 768px) {
    #menu-icon {
        display: block;
    }

    nav ul {
        display: none;
        flex-direction: column;
        align-items: center;
        background-color: #1f1268;
        width: 100%;
        margin-top: 0;
        padding: 10px 0;
    }

    #menu-toggle:checked + #menu-icon + nav ul { /* Affiche le menu quand le bouton est coché */
        display: flex;
    }

    nav li {
        margin: 10px 0;
    }

    nav a {
        font-size: 20px;
    }
}
</style>