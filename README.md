# Week5
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=no" />
    <title>Tutorial 1 - ArcGIS API for JavaScript - Display a map</title>

  <style>
      html,
      body,
      #viewDiv {
        padding: 0;
        margin: 0;
        height: 100%;
        width: 100%;
      }
  </style>

<link rel="stylesheet" href="https://js.arcgis.com/4.18/esri/themes/light/main.css">
<script src="https://js.arcgis.com/4.18/"></script>
  
 <script>
      require(["esri/config","esri/Map", "esri/views/MapView"], function (esriConfig,Map, MapView) 
  {
     esriConfig.apiKey = "AAPK0ffde8b49bd042d39fee7297dab05d93VJ343mJKhwXIKfh0G6HA4DgMIbfkwsxC9R_7TnVBGA6oy_JT9btyg4t7JGAr4tv7";

  const map = new Map({
   basemap: "arcgis-topographic" // 
       });
       
   const view = new MapView({
          map: map,
          center: [-118.805, 34.027], // 
          zoom: 13, // 
          container: "viewDiv" // 
        });

  });
  </script>
</head>
  <body>
    <div id="viewDiv"></div>
  </body>
</html>
