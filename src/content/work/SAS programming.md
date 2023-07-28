---
title: SAS programming
publishDate: 2020-03-02 00:00:00
img: /assets/stock-1.jpg
img_alt: Iridescent ripples of a bright blue and pink liquid
description: |
  The effect of student salaried work on academic success
tags:
  - Design
  - Dev
  - User Testing
---

<p style="text-align: justify;"><b>Objective: </b>In my previous professional experience with Les Grimpeurs, I had the opportunity to dissect the links between the economic situation in the USA and the financial support given to young Americans aspiring to a promising career. This prior experience fueled my curiosity to understand these crucial issues. I then set out to understand the reasons why French students choose to do paid work during their studies, whether or not in addition to receiving a scholarship, and what impact this has on their academic success.
While many students juggle academic responsibilities, they are also faced with the need to support themselves financially. However, a dilemma emerges: how to reconcile economic imperatives with academic commitment and ambitions for success?</p>

<img src="/assets/as-var.JPG">

<p style="text-align: justify;"><b>The Data: </b>Throughout this captivating study, we'll explore data from a sample of 46,340 students enrolled in French higher education between 2015 and 2016 and who responded to the L'OVE (Observatoire de la vie étudiante) survey. We will examine the consequences of this delicate balance between professional obligations and educational ambitions using the data provided by this survey. We therefore have a sample of 46340 observations and 15 columns with relevant control variables, as shown above.</p>

<img src="/assets/as-clean.JPG">

<p style="text-align: justify;"><b>Preparation of the database: </b>I carried out this study using SAS only. First, I perform initial data cleaning and processing operations to prepare the database for analysis. For example, in the image above, you can see that I create indicator variables for study-related jobs and non-study-related jobs, classifying them according to their weekly frequency. Or I organize individuals into different age brackets to facilitate statistical analysis. By adding the removal of extreme or missing values, this preparatory process will enable more in-depth analysis of the effect of student employment on academic achievement.</p>

<h5>Descriptive statistics</h5>

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
  <img src="/assets/as-sd1.JPG" alt="Description de l'image" onclick="openLightbox(this)" onmouseover="setHandCursor(this)">
    
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

<p style="text-align: justify;"><b>interpretations: </b>This table provides an overview of our sample and study population, taking into account student work, success in the first semester, as well as gender and age. Around 80% of students passed their first semester, while 20% unfortunately failed. Of these, the majority (68%) do not work outside their studies. Of those students who have a salaried job unrelated to their studies, 3.87% work full-time, 4.95% more than half-time, 9.45% less than half-time and 13.11% occasionally.
As for the composition of the group studied, women represent 63.40% of the sample, while men make up 36.60%. The age of the students falls into three categories, with the 19-20 age group being the largest (36%), followed by the 21-22 age group (25.80%) and the 16-18 age group (22.38%).</p>

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
  <img src="/assets/as-sd2.JPG" alt="Description de l'image" onclick="openLightbox(this)" onmouseover="setHandCursor(this)">
    
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


<p style="text-align: justify;"><b>interpretation of the contingency table: </b>This table informs us of the distribution between the frequency of student salaried work and
academic success. We can first note that we reject the hypothesis of non-autocorrelation with
the validation of the first semester for the variables "Full-time student salaried work" at the
5% threshold, and "More than half time student salaried work" at the 1% threshold. 82.53%
of the students with a full-time job validated their first semester. Contrary to what we might
have thought, having a full-time student job seems to be beneficial for academic success. It
even seems to be more beneficial to have a full-time job than a more than half-time job where
the success rate is only 75.58%. For the other variables, the hypothesis of no autocorrelation
with the validation of the semester is accepted according to the chi-square test. It is therefore
difficult to draw conclusions on these variables and we must remain vigilant with regard to
these results following reverse causality and as science says, correlation is not causality. </p>

<h5>Econometric study:</h5>

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
  <img src="/assets/as-reg.JPG" alt="Description de l'image" onclick="openLightbox(this)" onmouseover="setHandCursor(this)">
    
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

<p style="text-align: justify;"><b>interpretation of the bivariate probit model: </b>For the bivariate probit model using the qlim procedure, we set up two simultaneous equations using all the control variables seen previously in the DATA section. One explains the effect of paid work on academic achievement, the other explains the effect of student social aid on paid work, which is shown in the Appendix. According to the positive and significant correlation coefficient we can deduce that our two models evolve simultaneously and have dependent behaviours. Scholarships therefore have an influence on whether or not the student goes into paid employment. At the mean point, receiving social aid will increase the probability of not doing paid work by 5.1 percentage points; and decrease the probability of doing paid work (regardless of how often it is done) by about 1.2 percentage points at the mean point, all other things being equal. In addition, the variable of interest: student paid work is significant this time, showing that the model does explain an effect of student paid work on academic success. We can see that as the frequency of student employment increases, the marginal effect decreases, and with quite large values. For example, holding a casual salaried job at mid-term reduces the probability of validating the first semester by 15.8 probability points on average compared to not holding a job at all, at the 1% threshold, all other things being equal. The marginal effect for full-time salaried 30 Internal employment is more than twice as high, at 34.7 points.</p>

<p style="text-align: justify;">This study allowed me to clarify my vision concerning the potential causes of failure in the first semester of an academic year in higher education, regardless of the level and field of study. The bivariate probit model shows that student employment outside the university curriculum has a negative impact on the validation of the first semester, as the frequency of salaried work increases. The scholarship is a way for students to support themselves (food and housing) without having to earn money by working while studying. But some students escape the rule and work full time during their studies, which makes it difficult for them to keep up with their studies because they can only revise their courses in the evening after work. In order to increase the success rate of employed students, governmental measures should be adopted, such as adjusting school schedules for students in financial difficulty who are obliged to work, but also facilitating access to social aid, especially for foreign students who are new in the French administration.</p>