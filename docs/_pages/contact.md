---
layout: single
permalink: /contact
title: "Contact"
---

Site en cours de construction

 <div id="map"/>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css" integrity="sha512-Rksm5RenBEKSKFjgI3a41vrjkw4EVPlJ3+OiI65vTjIdo9brlAacEuKOiQ5OFh7cOI1bkDwLqdLw3Zg0cRJAAQ==" crossorigin="" />
<script src="https://unpkg.com/leaflet@1.3.1/dist/leaflet.js" integrity="sha512-/Nsx9X4HebavoBvEBuyp3I7od5tA0UzAxs+j83KgC8PU0kgB4XiK4Lfe4y4cgBtaRJQEIFCW+oC506aPT2L1zw==" crossorigin="">
</script>
<script type="text/javascript">
    // On initialise la latitude et la longitude de Paris (centre de la carte)
    var lat = 47.15432488494391;
    var lon = -1.5232560503890042;

    var latlngs = [
        [47.13906217626143, -2.1163869066697214],
        [47.25536358313592, -1.5981426763155702],
        [47.211780427615096, -1.1749891304300706],
        [46.91219064842252, -1.189252733100368],
        [46.855322087773246, -1.8715283941629433]
    ];
    var myMap = null;
    // Fonction d'initialisation de la carte
    function initMap() {
        myMap = L.map('map').setView([lat, lon], 10);
        // Leaflet ne récupère pas les cartes (tiles) sur un serveur par défaut. Nous devons lui préciser où nous souhaitons les récupérer. Ici, openstreetmap.fr
        L.tileLayer('https://{s}.tile.openstreetmap.fr/osmfr/{z}/{x}/{y}.png', {
            // Il est toujours bien de laisser le lien vers la source des données
            attribution: 'données © <a href="//osm.org/copyright">OpenStreetMap</a>/ODbL - rendu <a href="//openstreetmap.fr">OSM France</a>',
            minZoom: 1,
            maxZoom: 20
        }).addTo(myMap);
        var polygon = L.polygon(latlngs, {color: 'blue'});
        polygon.addTo(myMap);

        /*
        var circleOptions = {
            color: 'blue',
            fillColor: 'blue'
        };
        var circleCenter = [lat, lon];
        var circle = L.circle(circleCenter, 20000, circleOptions);
        circle.addTo(myMap);*/
    }
    window.onload = function(){
        initMap(); 
    };
</script>