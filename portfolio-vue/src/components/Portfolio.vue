<template>
  <div class="portfolio">

    <!-- Menu mobile -->
    <input type="checkbox" id="menu-toggle">
    <label for="menu-toggle" id="menu-icon">&#9776;</label>
    <nav>
      <ul>
        <li><a href="#aPropos">À propos</a></li>
        <li><a href="#softSkills">Soft Skills</a></li>
        <li><a href="#technologies">Technologies</a></li>
        <li><a href="#realisations">Réalisations</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <header>
      <section id="banner">
        <img src="@/assets/test.png" id="pp3" alt="Photo de profil" />
        <section id="topPresentation">
          <h1>Samir Ziani</h1>
          <p id="p1">
            Étudiant en BTS SIO (Services Informatiques aux Organisations)
          </p>
        </section>
      </section>
    </header>
    <section id="separateur"></section>
    <section id="sections">
      <!-- À propos -->
      <section id="aPropos">
        <h2>À propos</h2>
        <p>
          Je m’appelle Samir ZIANI, et mon parcours est celui d’une évolution guidée par la curiosité et l’envie d’apprendre.
          Après des études en économie et gestion, j’ai progressivement ressenti le besoin de me rapprocher d’un domaine plus concret.
          Aujourd’hui, je poursuis cette reconversion avec enthousiasme en préparant un BTS SIO à Strasbourg. Chaque jour, j’y
          découvre un peu plus la richesse de ce domaine entre réseaux, systèmes, nouvelles technologies, et cela renforce ma
          conviction d’avoir trouvé ma voie.
        </p>
      </section>
      <!-- Soft Skills -->
      <section id="competences">
        <section id="softSkills">
          <img src="@/assets/softskills.png" id="softskills1" alt="Image soft skills">
          <section id="softSkillsContent">
            <h2>Soft Skills</h2>
            <section id="colonneSoft">
              <ul>
                <li><img src="@/assets/adaptation.png" id="adaptation" alt="Capacité d'adaptation">Capacité d'adaptation</li>
                <li><img src="@/assets/relationclient.png" id="relationclient" alt="Créatif">Créatif</li>
                <li><img src="@/assets/autodidacte.png" id="autodidacte" alt="Autodidacte">Autodidacte</li>
              </ul>
              <ul>
                <li><img src="@/assets/analytique.png" id="analytique" alt="Esprit analytique">Esprit analytique</li>
                <li><img src="@/assets/persuasion.png" id="persuasion" alt="Force de persuasion">Force de persuasion</li>
                <li><img src="@/assets/equipe.png" id="equipe" alt="Travail en équipe">Travail en équipe</li>
              </ul>
            </section>
          </section>
        </section>
        <!-- Technologies -->
        <section id="technologies">
          <img src="@/assets/technologies.png" id="technologies1" alt="Image technologies">
          <section id="technologiesContent">
            <h2>Technologies</h2>
            <section id="colonneTech">
              <ul>
                <li><img src="@/assets/codage.png" id="codage" alt="HTML et CSS">HTML et CSS</li>
                <li><img src="@/assets/javascript.png" id="javascript" alt="JavaScript, MySQL">JavaScript, MySQL</li>
              </ul>
              <ul>
                <li><img src="@/assets/windows.png" id="windows" alt="Windows">Windows, migration</li>
                <li><img src="@/assets/ordinateur.png" id="ordinateur" alt="Montage PC">Montage, installation et configuration de postes de travail</li>
              </ul>
            </section>
          </section>
        </section>
        <!-- Réalisations -->
        <section id="realisations">
          <img src="@/assets/realisations.png" id="realisations1" alt="Image réalisations">
          <section id="realisationsContent">
            <h2>Réalisations</h2>
            <section id="realisationsColonne">
              <p>Création de mon Portfolio en 2025 avec HTML et CSS</p>
              <p>Virtualisation d'un serveur et configuration d'un environnement Active Directory</p>
            </section>
          </section>
        </section>
      </section>
      <!-- Contact -->
      <section id="contact">
        <section id="contactContainer">
          <!-- Colonne gauche -->
          <section id="contactInfo">
            <h2>Contact</h2>
            <p>Vous pouvez me contacter ou consulter mes profils :</p>
            <ul>
              <li><a href="https://www.linkedin.com/in/samir-ziani-2ab651154/" target="_blank">LinkedIn</a></li>
              <li><a href="https://github.com/SamirZNI" target="_blank">GitHub</a></li>
            </ul>
            <p>Vous pouvez aussi m’envoyer un mail directement en cliquant 
              <a href="mailto:samir.zn7@gmail.com">ici</a>.
            </p>
          </section>
          <!-- Colonne droite -->
          <section id="contactCV">
            <h3>Mon CV</h3>
            <a href="@/assets/CV_Samir.pdf" download>
              <img src="@/assets/cv.png" id="cvImage" alt="Aperçu CV Samir ZIANI">
            </a>
            <p>Vous pouvez télécharger mon CV en cliquant sur l'icône ci-dessus</p>
          </section>
        </section>
      </section>
    </section>
    <footer>
        <p>2025 Samir ZIANI. Tous droits réservés.</p>
    </footer>
  </div>
</template>


<script>
export default { 
  data() { 
    return {
      message: "Bienvenue sur mon portfolio Vue !",
    };
  },
};
</script>


<style>
html {
    scroll-behavior: smooth;
}
body {
    background-image: url("@/assets/background3.jpg");
    background-color: #5642c7;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    width: 100%;
}
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
    z-index: 1000;
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
#sections {
    line-height: 1.5;
}
#aPropos {
    display: block;
    color: #e2e7ff;
    background-color: #402ea8b7;
    line-height: 1.72;
    font-size: 20px;
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.459);
    margin: 50px;
    padding: 40px;
    text-align: center;
    justify-content: center;
    opacity: 0;
    transform: scale(0.9) translateY(40px);
    animation: zoomInSmooth 1s ease-out both;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
}
#aPropos h2 {
    background-color: #301c9e;
    border-radius: 8px;
    box-shadow: #000000 1px 1px 2px;
    padding: 5px 100px;
    display: inline-block; /* Pour que le fond ne prenne que la largeur du texte */
}
#aPropos p {
    text-align: justify; /* bien carré, aligné à gauche et à droite */
    text-align-last: center; /* dernière ligne centrée */
}
/* Animation */
@keyframes zoomInSmooth {
  from {
    opacity: 0;
    transform: scale(0.7) translateY(40px);
  }
  to {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}
#competences {
    display: flex;
    gap: 20px;              /* espace entre les colonnes */
    padding: 40px;
    justify-content: space-between;
    align-items: stretch;
}
/* Chaque section à l’intérieur prend la même largeur */
#softSkills,
#technologies,
#realisations {
    position: relative; /* sur chaque section, les images flottantes sont centrées par rapport au bloc (pour positionner l’image flottante) */
    background-color: #402ea8b7;
    color: #e2e7ff;
    border-radius: 15px;
    padding: 50px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.45);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    text-align: center;
    width: 32%;        
    /* Animation douce */
    opacity: 0;
    transform: scale(0.85) translateY(40px); /* position et taille de départ, 0.85 c'est : l'élément est à 85% de sa taille à l'apparition puis devient taille normal au fur et à mesure en plein centre de l'écran, et translateY(40px), il est déplacé vers le bas de 40 px. */
    animation: zoomInSmooth 4s ease-out both;  /* l'élément commence vite et finit doucement en 1 seconde */
    animation-timeline: view(); /* l'animation se déclenche au fur et à mesure que l’élément entre dans le champ de vision.*/
    animation-range: entry 0% cover 50%; /* l'animation commence dès que l’élément commence à entrer dans le champ de vision (entry 0%) et se termine lorsque 50% de l’élément est visible (cover 50%) */
}
/* Animation douce */
@keyframes zoomInSmooth {
    from {
        opacity: 0;
        transform: scale(0.85) translateY(40px); 
    }
    to {
        opacity: 1;
        transform: scale(1) translateY(0);
    }
}
/* Colonnes internes pour listes (Soft Skills et Technologies) */
#colonneSoft,
#colonneTech {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
}

/* Listes internes */
#colonneSoft ul,
#colonneTech ul {
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: left;
}
#colonneSoft li,
#colonneTech li {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
}
#colonneSoft li img,
#colonneTech li img {
    width: 50px;
    height: 50px;
    object-fit: cover;
    border-radius: 10px;
    margin-right: 10px;
}

/* Image flottante au-dessus du bloc */
#softskills1,
#technologies1,
#realisations1 {
    position: absolute;
    top: -60px;           /* sort au-dessus du bloc */
    left: 50%;            /* centre horizontalement */
    transform: translateX(-50%); /* centre parfaitement, ici déplace l'image vers la gauche de 50% de sa propre largeur */
    width: 42%;        /* taille adaptée */
}
#realisations1 {
    width: 35%;       
    border-radius: 25px;
}
#softSkillsContent,
#technologiesContent,
#realisationsContent {
    padding-top: 60px; 
    font-size: 19px;
}

#contact {
    color: #e2e7ff;
    justify-content: center;
    background-color: #27257cd5;
    font-size: 20px;
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(7, 0, 34, 0.459);
    margin: 50px;
    padding: 30px;
}

/* Conteneur interne : 2 colonnes centrées */
#contactContainer {
    display: flex;
    gap: 100px;               /* espace entre les colonnes */
    justify-content: center;  /* centre les colonnes horizontalement */
    align-items: flex-start;
    max-width: 80%;         /* largeur maximale du conteneur */
    margin: 0 auto;           /* centre le conteneur dans le bloc bleu */
}

/* Liste des liens */
#contact ul {
    list-style: none; 
    padding: 25px 0;           
    display: flex;
    justify-content: center;   /* centre les boutons horizontalement */
    gap: 20px;
}

/* Boutons LinkedIn / GitHub */
#contact ul li a {
    text-decoration: none;
    color: #e2e7ff;
    padding: 8px 20px;
    border-radius: 25px;
    font-weight: bold;
    transition: all 0.3s ease;
    box-shadow: 0 4px 10px rgba(0,0,0,0.3);
}
#contact ul li a[href*="linkedin"] {
    background-color: #0077b5;
}
#contact ul li a[href*="github"] {
    background-color: #333;
}
#contact ul li a:hover {
    transform: scale(1.1);
    box-shadow: 0 6px 20px rgba(0,0,0,0.5);
    filter: brightness(1.2);
    transition: all 0.3s ease;
}
#cvImage {
    width: 90px;
    height: 90px;
    display: block;
    margin: 10px auto;
}
#cvImage:hover {
    transform: scale(1.07);
    filter: brightness(1.1);
    transition: all 0.3s ease;
}
#contactCV h3 {
    color: #e2e7ff;
    border-radius: 8px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bold;
    font-size: 40px;
    text-shadow: #000000 1px 1px 2px; 
    text-align: center;
}
#contactInfo h2 {
    color: #e2e7ff;
    border-radius: 8px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bold;
    font-size: 40px;
    text-shadow: #000000 1px 1px 2px; 
    text-align: center;
}
footer {
    background-color: #0b0836;
    color: #e2e7ff;
    text-align: center;
    padding: 1px ;
}




h2 {
    color: #e2e7ff;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bold;
    font-size: 40px;
    text-shadow: #000000 1px 1px 2px;   
}
</style>