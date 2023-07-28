---
title: Python Data visualization
publishDate: 2019-10-02 00:00:00
img: /assets/stock-4.jpg
img_alt: Soft pink and baby blue water ripples together in a subtle texture.
description: |
  Data visualization project to determine the ideal period for surfing the waves at Mooloolaba in Australia.
tags:
  - Design
  - Branding
---

<!DOCTYPE html>
<html>
<head>
    <title>Image à gauche, texte à droite</title>
    <style>.container {display: flex;}
    .text {
            flex: 1; /* La deuxième colonne prendra la moitié de l'espace disponible */
            text-align: justify; }/* Justifier le texte */
        .image {
            flex: 1; /* La première colonne prendra la moitié de l'espace disponible */
            padding-right: 20px; /* Espacement entre l'image et le texte */
        }
        .image img {
            max-width: 100%; /* L'image occupera 100% de la largeur de la première colonne */
            height= "850";
            width="1500"; /* La hauteur de l'image sera ajustée proportionnellement */
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="image">
            <img src="/assets/db-waves.JPG" alt="Image à gauche">
        </div>
        <div class="text">
            <p><b>The objective:</b> For my exciting upcoming surfing adventure at Mooloolaba, Australia, I decided to embark on a data exploration journey. To achieve this, I obtained a dataset from the Kaggle website, generously provided by the Queensland government, which contains valuable meteorological data relating to wave size at Mooloolaba. My ultimate aim is to use this data to determine the optimum period for catching the best waves at this renowned surfing spot.</p>
            <br>
            <p><b>The Data:</b> The data provided runs from January 1, 2017 at 00:30 to June 30, 2019 at 23:30. This dataset has 7 columns: minimum and maximum height, periods, direction and water temperature. Each row corresponds to data for the last 30 minutes. In order to analyze the data, I decided to import this csv file into Jupyter. The aim was firstly to explore the data and analyze the evolution of weather conditions on the surf spot.</p>
        </div>
    </div>
</body>
</html>




<html>
<body>
  <img src="/assets/1-waves.JPG" alt="Image 1">
</body>
</html>


<!DOCTYPE html>
<html>
<head>
    <title>Double Justification</title>
    <style>
        p {
            text-align: justify;
          }
    </style>
</head>
<body>
    <p><b>The libraries:</b> After launching Anaconda and Jupyter Notebook, I import the libraries that I will need: Pandas, NumPy, Seaborn, and Matplotlib. Pandas and NumPy are convenient for manipulating and analyzing data in a simple and intuitive way. Pandas allows us to read and write files in various formats such as csv, txt, xls, sql, etc. Numpy provides operations for data processing that make its use easier. Seaborn and Matplotlib will be used for data visualization purposes, allowing us to create bar charts, matrices, and more.</p>
    <p><b>Exploration of the Data:</b> I examine the initial 5 rows of my CSV file by utilizing df.head(). Upon observation, I observe a well-balanced distribution of data across the 7 columns, each of them containing valuable information. To gain deeper insights into the file, I employ df.info() to identify any null, missing, or unprocessed data that might potentially impact the accuracy of my analysis.
    I observe that only the Date/Time column needs to be reprocessed to inform Python that it represents temporal data. As for the variables related to wave characteristics (height, frequency, direction), their data type remains unchanged.</p>


    
</body>
</html>



<html>
<body>
  <img src="/assets/2-waves.JPG" alt="Image 1" width="500" height="100">
</body>
</html>


<p><b>Data clean-up:</b> after noticing the existence of negative values for water temperature, wave size and frequency (which is physically impossible), I decide to delete the lines containing these errors. I also create a dictionary containing the months and convert Date/Time into a python-readable datetime time object using the datetime library.</p>

<html>
<body>
  <img src="/assets/3-waves.JPG" alt="Image 1" width="500" height="100">
</body>
</html>

<p><b>sample statistics:</b></p>
<p>-Hmax: maximum wave record over the period</p>
<p>-Hs: Significant wave height (highest third)</p>
<p>-Tz, Tp: period of rising waves (Tz) and peak energy (Tp)</p>
<p>-SST and Peak direction: Water surface temperature and wave direction.</p>
<p>At Mooloolaba, Australia, the average wave height is 1.21 meters, which is close to the median (1.10). The difference is probably due to the presence of extreme (and rare) values: sometimes waves reach 7.26 meters during storms and high tides. But with an average surface temperature of 23.7°C and a low dispersion (std=2.23°C), the water is good almost all the time.</p>




<!DOCTYPE html>
<html>
<head>
    <title>Image à gauche, texte à droite</title>
    <style>.container {display: flex;}
    .text {
            flex: 1; /* La deuxième colonne prendra la moitié de l'espace disponible */
            text-align: justify; }/* Justifier le texte */
        .image {
            flex: 1; /* La première colonne prendra la moitié de l'espace disponible */
            padding-right: 20px; /* Espacement entre l'image et le texte */
        }
        .image img {
            max-width: 100%; /* L'image occupera 100% de la largeur de la première colonne */
            height= auto; /* La hauteur de l'image sera ajustée proportionnellement */
        }
    </style>
</head>

<h5>data cross-referencing:</h5>

<body>
    <div class="container">
        <div class="image">
            <img src="/assets/4-waves.JPG" alt="Image à gauche">
        </div>
        <div class="text">
            <p>This code will draw a diagram representing the average wave height during each month of 2017 and 2018. This will enable us to determine the months of the year when the Mooloolaba Sea is most generous in terms of wave height for surfers.</p>
        </div>
    </div>
</body>
</html>



<html>
<body>
  <img src="/assets/5-waves.JPG" alt="Image 1" width="500" height="100">
</body>
</html>

<p><b>Bar chart:</b> The months of the year with the highest average wave size are March and April, when the average wave size is around 1.60 meters. The ocean seems much calmer in July, August and September, with an average wave size of 0.8 meters - not enough to capsize a ship. Ideally, we'd like to get our boards out around March-April.</p>

<html>
<body>
  <img src="/assets/7-waves.JPG" alt="Image 1" width="500" height="100">
</body>
</html>

<p><b>continuous variable graph: </b>By plotting the evolution of the water temperature between early 2017 and 2019, we can determine when the more chilly among us will be able to get out his board. Looking at 2017 and 2018, we can see that the sea is warmest at the beginning of the year: between February and April. Chilly people are in luck, as they'll enjoy big waves and warm water. </p>

<html>
<body>
  <img src="/assets/6-waves.JPG" alt="Image 1" width="500" height="100">
</body>
</html>

<p><b>Cross tabulation:</b> The 1.60 m waves of March and April certainly offer the thrills that many surfers appreciate. However, it's interesting to note that some intrepid surfers, known as big wave riders, are attracted by far more impressive challenges. They can catch waves reaching heights of 5, even 10 meters, to push their limits and enjoy unique experiences in the heart of the Pacific Ocean. 
After adding an indicator variable for wave size, we can see that, although rare, there were waves in October (21) whose size exceeded 6 meters (indicated by the number 4)</p>


<html>
<body>
  <img src="/assets/8-waves.JPG" alt="Image 1" width="500" height="100">
</body>
</html>


<p><b>Interval evolutions:</b> For safety reasons, it's a good idea to analyze the relationship between maximum wave height and wave period: the time elapsed between two successive waves. Using Seaborn's joinplot function, we have the relationship between our two continuous variables: Tz and Hmax. From the graph, we can see that the higher the waves, the higher is the lower bound of their period. For example, for a wave height of 5 meters, we have more than around 6.3 seconds minimum to get to the surface. That's a good point because we're more likely to have time to catch our breath before another big wave breaks over us.</p>
<br>
<p><b>Conclusion: </b>The ideal period for amateur surfers is March and April, when the waves are fairly high and the water around 28 degrees Celsius. However, in rare cases during the month of October, when swells are strong, some giant waves can exceed 6 meters. Although the water is cooler (21 degrees), conditions are ideal for the most seasoned surfers looking for a thrill. </p>