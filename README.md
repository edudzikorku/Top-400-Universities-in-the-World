<!DOCTYPE html>
<html lang="eng">
    <head>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <h1>Population Distribution Among The Top 400 Universities in The World</h1>
        &#160;
        <h4><a  href="https://youtu.be/fhEnYUDsYd0 ">Video Demo:</a></h4>
        &#160;
        <h4>Dscription:</h4>
        <h5><b>Overview</b></h5>
            <p>
                In the recent world university rankings by the Times Higher Education, <b>four</b> universities from Africa were part of the first 400.
                <cite>The <a href="https://www.timeshighereducation.com/world-university-rankings/2023/world-ranking">Times Higher Education World University Rankings 2023</a> include 1,799 universities across 104 countries and regions, making them the largest and most diverse university rankings.
                The table is based on 13 carefully calibrated performance indicators that measure an institution’s performance across four areas: teaching, research, knowledge transfer and international outlook.
                In 2022, the ranking analysed over 121 million citations across more than 15.5 million research publications and included survey responses from 40,000 scholars globally. Overall, at least 680,000 datapoints were collected from more than 2,500 institutions that submitted data.
                Trusted worldwide by students, teachers, governments and industry experts, the league table revealed how the global higher education landscape is shifting.
                The topmost portion of the list was occupied by the University of Oxford. This was followed by Harvard University. The University of Cambridge jumped from joint fifth from the previous year to joint third.
                The highest new entry was Italy’s Humanitas University, ranked in the 201-250 bracket.
                The US was the most-represented country overall, with 177 institutions, and also the most represented in the top 200 (58).
                Mainland China had the fourth-highest number of institutions in the top 200 (11, compared with 10 in the previous year), having overtaken Australia, which had dropped to fifth (joint with the Netherlands).
                For the first time, five countries - all in Africa (Zambia, Namibia, Mozambique, Zimbabwe and Mauritius) entered the ranking. While Harvard topped the teaching pillar, Oxford led the research pillar.
                Atop the international pillar was the Macau University of Science and Technology.</cite>
            </p>
                &#160;
            <p>With this, the project sought to display the information on a web map.</p>
        <h5><b>Data Analysis And Visualization</b></h5>
            <p>
                The entire project was executed in <a href="https://colab.research.google.com/">Google Colab</a>.
                Data was downloaded (in a json format) from the above site, using the python package <a href="https://docs.python.org/3/library/urllib.html">urllib</a>. This was later converted to a <a href="https://pandas.pydata.org/">pandas</a> dataframe for further processing. Although the site provided the home countries, it missed the geolocations of the institutions. Hence the <a href="https://nominatim.org/">Nominatim</a> geocoding service was adopted to geocode the institutions. The geocoded data was then transformed into a <a href="https://geopandas.org/en/stable/">geopandas</a> dataframe. Finally, <a href="https://python-visualization.github.io/folium/">Folium</a> was used to display the geolocated data on a map. Two interactive web maps were produced; the first one represented the student population densities of the institutions, using graduated symbols, while the second map showed actual locations of the institutions. Unfortunately, a legend was not added to the graduated symbols map, since the folium library does not have this capability at the moment
            </p>
        <h5><b>Project files</b></h5>
            <p>
            The files used for the project include a jupyter notebook, a json file, two csv files, and two html files.
            The notebook contains the codes used for the project. The json file contains the raw data downloaded from Times Higher Education. The csv files contain the institutions, one without coordinates, and one with coordinates.The html files are the web maps.
            </p>
        <h5><b>Usage</b></h5>
            <p>
            Open any of the html files in a web browser to visualize the information it contains. You can search for a university, using the search button. To change the base map, use the layer control button at the top right to select your prefered base map.
            </p>
    </body>
</html>
