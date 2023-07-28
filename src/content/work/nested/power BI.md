---
title: Power BI
publishDate: 2020-03-04 00:00:00
img: /assets/stock-3.jpg
img_alt: Pearls of silky soft white cotton, bubble up under vibrant lighting
description: |
  Statistical study of scholarships in the US between 2000 and 2019.
tags:
  - Design
  - Dev
  - Branding
---

<p><b>Context:</b> "Les Grimpeurs" is a start-up providing assistance to international students in their search for scholarships. 
When I joined the company as a Data Analyst, my first project was to populate and clean a database with the terms and conditions of each American scholarship in partnership with the company.
Then, my objective was to study the evolution of the American scholarship market to verify whether it is growing or not.</p>



<!DOCTYPE html>
<html>
<head>
    <title>Afficher une image en grand avec Lightbox et un curseur personnalisé</title>
    <style>
        /* Styles pour la lightbox */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 9999;
        }
        .lightbox img {
            display: block;
            margin: 50px auto; /* Ajustez la marge pour centrer l'image */
            max-width: 90%;
            max-height: 80%;
        }
        /* Style pour le bouton de fermeture */
        .close-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    
  <!-- Insérez l'image en utilisant la balise <img> avec les attributs onclick et onmouseover -->
  <img src="/assets/sc-data.JPG" alt="Description de l'image" onclick="openLightbox(this)" onmouseover="setHandCursor(this)">
    
  <!-- Lightbox -->
  <div class="lightbox" onclick="closeLightbox()">
        <span class="close-btn">&times;</span>
        <img src="" alt="Image en grand">
    </div>

   <!-- Script JavaScript pour gérer la lightbox et le curseur personnalisé -->
   <script>
        function openLightbox(image) {
            var lightbox = document.querySelector(".lightbox");
            var imageToShow = lightbox.querySelector("img");
            imageToShow.src = image.src;
            lightbox.style.display = "block";
        }

        function closeLightbox() {
            var lightbox = document.querySelector(".lightbox");
            lightbox.style.display = "none";
        }

        function setHandCursor(image) {
            image.style.cursor = "pointer";
        }
    </script>
</body>
</html>

<p><b>The Data:</b> The main difficulty was to find by combining several sources. The first from the Statista website, which shows changes in the number of students, total spending on higher education, and the amount of student aid. Then I used the Country Economy and OECD websites for purchasing power trends (inflation rate and GDP per capita) between 2000 and 2019. I then arranged the data and pre-processed it using power BI.</p>

<h5>Dashboard using Power BI:</h5>


<!DOCTYPE html>
<html>
<head>
    <title>Afficher une image en grand avec Lightbox et un curseur personnalisé</title>
    <style>
        /* Styles pour la lightbox */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 9999;
        }
        .lightbox img {
            display: block;
            margin: 50px auto; /* Ajustez la marge pour centrer l'image */
            max-width: 90%;
            max-height: 80%;
        }
        /* Style pour le bouton de fermeture */
        .close-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    
  <!-- Insérez l'image en utilisant la balise <img> avec les attributs onclick et onmouseover -->
  <img src="/assets/sc-BI.JPG" alt="Description de l'image" onclick="openLightbox(this)" onmouseover="setHandCursor(this)">
    
  <!-- Lightbox -->
  <div class="lightbox" onclick="closeLightbox()">
        <span class="close-btn">&times;</span>
        <img src="" alt="Image en grand">
    </div>

   <!-- Script JavaScript pour gérer la lightbox et le curseur personnalisé -->
   <script>
        function openLightbox(image) {
            var lightbox = document.querySelector(".lightbox");
            var imageToShow = lightbox.querySelector("img");
            imageToShow.src = image.src;
            lightbox.style.display = "block";
        }

        function closeLightbox() {
            var lightbox = document.querySelector(".lightbox");
            lightbox.style.display = "none";
        }

        function setHandCursor(image) {
            image.style.cursor = "pointer";
        }
    </script>
</body>
</html>

<p><b>Dashboard 1:</b> The total cost spent by students on their studies seems to be growing faster than the total amount the state allocates to grants. We also note that 16.82% of total study costs are financed by student grants. This is probably because only the most deserving students in financial difficulty are more likely to receive a grant.</p>

<p>The number of students seems to have remained relatively stable between 2000 and 2019, with a slight increase from 2009 onwards. This increase is small compared with the amount allocated to student grants, which rose sharply between 2008 and 2010. There is a real financial investment on the part of the United States to help students finance their studies.</p>


<!DOCTYPE html>
<html>
<head>
    <title>Afficher une image en grand avec Lightbox et un curseur personnalisé</title>
    <style>
        /* Styles pour la lightbox */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 9999;
        }
        .lightbox img {
            display: block;
            margin: 50px auto; /* Ajustez la marge pour centrer l'image */
            max-width: 90%;
            max-height: 80%;
        }
        /* Style pour le bouton de fermeture */
        .close-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    
  <!-- Insérez l'image en utilisant la balise <img> avec les attributs onclick et onmouseover -->
  <img src="/assets/sc-infla.JPG" alt="Description de l'image" onclick="openLightbox(this)" onmouseover="setHandCursor(this)">
    
  <!-- Lightbox -->
  <div class="lightbox" onclick="closeLightbox()">
        <span class="close-btn">&times;</span>
        <img src="" alt="Image en grand">
    </div>

   <!-- Script JavaScript pour gérer la lightbox et le curseur personnalisé -->
   <script>
        function openLightbox(image) {
            var lightbox = document.querySelector(".lightbox");
            var imageToShow = lightbox.querySelector("img");
            imageToShow.src = image.src;
            lightbox.style.display = "block";
        }

        function closeLightbox() {
            var lightbox = document.querySelector(".lightbox");
            lightbox.style.display = "none";
        }

        function setHandCursor(image) {
            image.style.cursor = "pointer";
        }
    </script>
</body>
</html>

<p><b>Dashboard 2: </b>In addition, we can see that the average cost of higher education per student is rising very slightly, independently of GDP per capita, which is increasing, and of the inflation rate, which is highly unstable. This is good news, because even if the cost of education stagnates in comparison with rising purchasing power, the US government continues to help the poorest and most deserving students to finance their education.</p>
<p>The second graph highlights an interesting trend: the average scholarship per student increased significantly between 2008 and 2010, despite the subprime crisis. This clearly illustrates the US government's commitment to investing in student financial aid.</p>