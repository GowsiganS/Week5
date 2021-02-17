# Week5

<html>
  <head>
    <meta charset="utf-8" />
    <link rel="stylesheet" href="https://js.arcgis.com/4.18/esri/themes/light/main.css">
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


<script src="https://js.arcgis.com/4.18/"></script>
  
<script>
      require([
          "esri/config",
          "esri/Map",
          "esri/views/MapView",
          "esri/widgets/Locate",
          "esri/widgets/Track",
          "esri/Graphic" ], 
  
  function(
            esriConfig,
            Map,
            MapView,
            Locate,
            Track,
            Graphic

        )
  {
     esriConfig.apiKey = "AAPK0ffde8b49bd042d39fee7297dab05d93VJ343mJKhwXIKfh0G6HA4DgMIbfkwsxC9R_7TnVBGA6oy_JT9btyg4t7JGAr4tv7";
  
  
const map = new Map({
          basemap: "arcgis-navigation"
        });

 const view = new MapView({
          container: "viewDiv",
          map: map,
          center: [-40, 28],
          zoom: 2
        });

  const locate = new Locate({
          view: view,
          useHeadingEnabled: false,
          goToOverride: function(view, options) {
            options.target.scale = 1500;
            return view.goTo(options.target);
          }
        });
        view.ui.add(locate, "top-left");

  });
    </script>
</head>
  <body>
    <div id="viewDiv"></div>
  </body>
</html>
