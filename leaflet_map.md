---
title: "Making a Map With Leaflet"
author: "Matiki"
date: "October 29, 2018"
output: 
  html_document: 
    keep_md: yes
---



First we load the required libraries.

```r
library(leaflet)
library(dplyr)
```

Next we create the map object with the leaflet(), addTiles(), and addMarkers() 
functions. We'll set the latitude and longitude to Rosario, Argentina, the 
birthplace of the world's greatest soccer player: Lionel Messi.


```r
map <- leaflet() %>%
        addTiles() %>%
        addMarkers(lat = -32.9442, 
                   lng = -60.6505, 
                   popup = "Rosario, Argentina")
map
```

<!--html_preserve--><div id="htmlwidget-0070e32675b0d045cae5" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-0070e32675b0d045cae5">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[-32.9442,-60.6505,null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"Rosario, Argentina",null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[-32.9442,-32.9442],"lng":[-60.6505,-60.6505]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
