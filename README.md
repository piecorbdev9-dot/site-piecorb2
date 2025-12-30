# site-piecorb2
"Portfolio persor: HTML, CSS et JavaScript
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
   <title>Mon Portfolio</title>
   <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Piecorb</h1>
        <p>Développeur web débutant</p>

        <img src="images.img/SMB.jpeg" alt="Photo de profil" class="profile-img">
    </header>

    <section class="about">
        <h2>A propos de moi</h2>
        <p>
            Je suis un passionné du développement web.
            J'apprends HTML, CSS et JavaScript pas à pas.
        </p>
    </section>

    <section class="skills">
        <h2>Compétences</h2>
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript (bases)</li>
        </ul>
    </section>

    <section class="contact">
        <h2>Contact</h2>
       
        <form id="contactForm">
            <input type="text" id="name" placeholder="Votre nom"><br><br>
            <input type="email" id="email" placeholder="Votre email"><br><br>
            <button type="submit">Envoyer</button>
        </form>

        <p id="formMessage"></p>
    </section>

    <footer>
        <p>@ 2025 - Mon PORTFOLIO</p>
    </footer>
    
    <script src="script.js"></script>
</body>
</html>

# Portfolio - Saïdou Mballo

##  Description
Portfolio personnel créé avec HTML, CSS et JavaScript.
Ce projet montre mes bases en développement web et mon évolution.

## Technologies utilisées
- HTML5
- CSS3
- JavaScript

## Fonctionnalités
- Présentation personnelle
- Formulaire de contact avec validation
- Design responsive

## Auteur
Saïdou Mballo - Développeur Web Junior

## Statut du projet
Projet terminé et prêt pour la mise en ligne sur Github Pages.

const form = document.getElementById("contactForm");
const nameInput = document.getElementById("name");
const emailInput = document.getElementById("email");
const formMessage = document.getElementById("formMessage");

form.addEventListener("submit", function (e) {
    e.preventDefault();

    if (nameInput.value === "" || emailInput.value === "") {
        formMessage.textContent = "Tous les champs sont obligatoires";
        formMessage.style.color = "red";
    } else {
        formMessage.textContent = "Message envoyé avec succès";
        formMessage.style.color = "green";
        form.reset();
    }
});

document.addEventListener("DOMContentLoaded", function () {
    console.log("Portfolio chargé avec succès");
});
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #222;
    color: white;
    text-align: center;
    padding: 30px;
}

section {
    padding: 20px;
    margin: 20px;
    background: white;
    border-radius: 5px;
}

h2 {
    color: #222;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    background: #ddd;
    margin: 5px 0;
    padding: 8px;
    border-radius: 4px;
}

footer {
    text-align: center;
    padding: 15px;
    background: #222;
    color: white;
}

/* Boutons */
button {
    background-color: #007bff;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #0056b3;
}

/* Inputs */
input {
    width: 90%
    max-width 300px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

/* Contact section */
.contact {
    text-align: center;
}

/* Responsive design */
@media (max-width: 600px) {
    header {
        padding: 20px;
    }

    section {
        margin: 10px;
    }

    h1 {
        font-size: 22px;
    }
}

.profile-img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50%;
    margin-top: 15px;
}

section {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

section :hover {
    transform: scale(1.02);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}
