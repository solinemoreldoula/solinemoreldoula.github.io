---
layout: single
permalink: /accompagnements
title: "Accompagnements"
---

## Comment ça se passe ?

Je suis disponible pour un premier contact téléphonique, pour faire connaissance et que tu puisses me poser les questions que tu souhaites sur mon accompagnement. 
Les rendez-vous ont ensuite lieu à ton domicile, ou dans tout autre lieu où tu te sens bien, et durent environ 2h. 

Les rdv des forfaits sont à répartir entre la grossesse et le post-partum. Pendant cette période, je suis disponible par mail ou par téléphone. Je peux également te proposer un prêt de livres.

<div class="container">
  <div class="table-price">
    <div class="pic-item">
       <img src="/assets/images/doula/doula1.png"/>
    </div>
    <div class="description">
      <h1 class="title">RDV ponctuel</h1>
      <span class="price">70 € <br/>86 € libéral</span>
    </div>
  </div>
  <div class="table-price">
    <div class="pic-item">
      <img src="/assets/images/doula/doula2.jpg"/>
    </div>
    <div class="description">
     <h1 class="title">Forfait 5 RDV</h1>
      <span class="price">325 €   (soit 65 € /rdv) <br/>400 € libéral</span>
    </div>
  </div>
  <div class="table-price">
    <div class="pic-item">
     <img src="/assets/images/doula/doula3.jpg"/>
    </div>
    <div class="description">
      <h1 class="title">Forfait 10 RDV</h1>
      <span class="price"> 600 €   (soit 60 €/rdv)  <br/> 738 €  libéral</span>
    </div>
  </div>
  </div>

Paiement possible : 
<ul>
    <li> en libéral (chèques, virement bancaire) </li>
    <li> en CESU (classique ou préfinancé) uniquement pour les forfaits </li>
</ul>

Ma rémunération en tant que doula ne devrait pas être un obstacle à un accompagnement. Je suis ouverte si besoin pour en discuter.

<blockquote class="quote ">
<span>Bon cadeau </span> Parfois on ne sait pas quoi offrir d’utile à une amie ou à de futurs parents : un accompagnement doula est la bonne idée ! Selon votre budget, un forfait post natal ou un rendez-vous ponctuel, je m’adapte à ta demande
</blockquote>


Je suis installée en sud-Loire, près de Nantes, et je me déplace à ton domicile également sur la Vendée et une partie ouest du Maine et Loire. 




 <!-- Map -->
 <div id="map" ></div>
 <p>
<i>*Déplacement compris dans ma prestation ; au-delà de 20km de mon domicile, facturation de 0,60€/km (barème fiscal)  
.</i>
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



## En pratique, la différence entre le paiement en CESU et en libéral ?

Tu peux choisir de régler selon le régime libéral (tarifs de gauche). Aucune formalité supplémentaire dans ce cas.

Tu peux aussi choisir de régler en Chèques Emploi Service Universels (CESU, tarifs de droite). Tu es l’employeur et j’interviens en tant que salarié pour des services à la personne à domicile. La déclaration est à faire sur [le site de l’URSSAF](https://www.cesu.urssaf.fr/info/accueil/s-informer-sur-le-cesu/tout-savoir/c-est-quoi-pour-qui.html).
En utilisant le CESU, tu peux bénéficier d’un avantage fiscal pour les dépenses engagées pour l’emploi d’un salarié à domicile.

Tu peux te simplifier les choses en optant pour le CESU+ : tu délègues alors le processus de rémunération (prélevé directement sur ton compte une fois les coordonnées bancaires saisies). Mon bulletin de salaire est généré automatiquement, il n’y a qu’une seule déclaration à faire en fin de mois. Ce service est gratuit et accessible à tous.

Quelques comités d’entreprise, mutuelle, conseil départemental, proposent des CESU pré-financés (maintenant appelés Titres spéciaux de paiement). Je suis toujours salariée dans le cadre du service à la personne à domicile, le processus de déclaration à l’URSSAF est le même. 
