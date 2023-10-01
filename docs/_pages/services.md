---
layout: single
permalink: /services
title: "Mes accompagnements et tarifs"
---

Comment ça se passe ?

Je suis disponible pour un premier contact téléphonique, pour faire connaissance et que tu puisses me poser les questions que tu souhaites sur mon accompagnement. 

Les rendez-vous ont ensuite lieu à ton domicile, ou dans tout autre lieu où tu te sens bien, et durent environ 2h. 

RDV ponctuel, selon tes besoins et la période de vie que tu traverses :  75 €

Les rdv des forfaits sont à répartir entre la grossesse et le post-partum. Pendant cette période, je suis disponible par mail ou par téléphone. Je peux également te proposer un prêt de livres.

Forfait 5 RDV : 350 €   (soit 70 € /rdv)

Forfait 10 RDV : 650 €   (soit 65 €/rdv)


*** inclure possibilité de bons cadeaux ***


Paiement possible en libéral (chèques ou espèces) ou en CESU ????? (uniquement préfinancé ?) 


”Mes tarifs ne doivent pas être un frein pour te faire accompagner, je suis ouverte pour en discuter.” => à reformuler


Je suis installée en sud-Loire, près de Nantes, et je me déplace à ton domicile également sur la Vendée et une partie ouest du Maine et Loire. 


 <!-- Map -->
 <div id="map" ></div>
 <p>
<i>*Je me déplace gratuitement dans un rayon de 20km autour de mon domicile. Au delà, mes tarifs incluent des frais kilométriques.</i>
</p>

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
        var polygon = L.polygon(latlngs, {color: '#1f5595'});
        polygon.addTo(myMap);

        var elMarker = L.marker([lat, lon]);
        elMarker.bindTooltip("Mon domicile*", 
            {
                permanent: true, 
                direction: 'right'
            });
        elMarker.addTo(myMap);

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
