---
layout: single
permalink: /accompagnements
title: "Accompagnements"
---

## Comment ça se passe ?

Je suis disponible pour un premier contact téléphonique, pour faire connaissance et que tu puisses me poser les questions que tu souhaites sur mon accompagnement. 
Les rendez-vous ont ensuite lieu à ton domicile, ou dans tout autre lieu où tu te sens bien, et durent environ 2h. 
Selon tes besoins et la période de vie que tu traverses, je suis là pour te soutenir face à une problématique précise, répondre à un besoin d’information ou simplement t’offrir un espace d’écoute libre et sans jugement. Pour savoir comment se déroulent les rendez-vous, je t'invite à consulter [cette page](/doula).

<div class="container">
  <div class="table-price">
    <a href="mailto:solinemoreldoula@gmail.com">
    <div class="pic-item">
       <img src="/assets/images/accompagnements/1.jpg"/>
    </div>
    <div class="description">
      <h1 class="title">RDV ponctuel</h1>
      <span class="price">86 € libéral</span>
    </div>
    </a>
  </div>
  <div class="table-price">
    <a href="mailto:solinemoreldoula@gmail.com">
    <div class="pic-item">
      <img src="/assets/images/accompagnements/2.jpg"/>
    </div>
    <div class="description">
     <h1 class="title">Forfait 5 RDV</h1>
      <span class="price">325 €   (soit 65 € /rdv) <br/>400 € libéral</span>
    </div>
    </a>
  </div>
  <div class="table-price">
    <a href="mailto:solinemoreldoula@gmail.com">
    <div class="pic-item">
     <img src="/assets/images/accompagnements/3.jpg"/>
    </div>
    <div class="description">
      <h1 class="title">Forfait 10 RDV</h1>
      <span class="price"> 600 €   (soit 60 €/rdv)  <br/> 738 €  libéral</span>
    </div>
    </a>
  </div>
  </div>


Les accompagnements plus longs nous permettent de créer un lien de confiance durable. Dans le cadre d’une grossesse par exemple, nous avons le temps d’aborder différentes thématiques selon tes demandes (le déclenchement, la péridurale, allaitement ou biberon, le post-partum, le sommeil, le portage, la reprise du travail, le sevrage…).  Les rendez-vous des forfaits peuvent être répartis entre la grossesse et le post-partum. Pendant cette période, je suis disponible par mail ou par téléphone. Je peux également te proposer un prêt de livres.

## Pour le règlement ?


Paiement possible : 
<ul>
    <li> en libéral (chèques, virement bancaire) </li>
    <li> en CESU (classique ou préfinancé) uniquement pour les forfaits </li>
</ul>

Ma rémunération en tant que doula ne devrait pas être un obstacle à un accompagnement. Je suis ouverte si besoin pour en discuter.

<blockquote class="quote ">
<span>Bon cadeau </span> Parfois on ne sait pas quoi offrir d’utile à une amie ou à de futurs parents : un accompagnement doula est la bonne idée ! Selon ton budget, un forfait post natal ou un rendez-vous ponctuel, je m’adapte à ta demande
</blockquote>

## Secteur de déplacement

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
      // nord loire au dessus de la chapelle / erdre 
      [47.31664721641413, -1.5445540016466892],
      // orvault
      [47.272962724234, -1.6293870881578993],
      // st herblain
      [47.20906403165871, -1.6665625169979184],
      // indre 
      [47.19535680833296, -1.680005461179651],
      // corsept
      [47.27651899430666, -2.0748051736599065],
      // pornic
      [47.11321602338254, -2.114630614267812],
      // beauvoir sur mer 
      [46.91133630797509, -2.0472775785391284],
      // challans
      [46.82260919288586, -1.8831693014160147],
      // la roche /yon
      [46.650016349253185, -1.4306499888826807],
      // les herbiers
      [46.85840648278568, -1.0042484212822218],
      // cholet
      [47.05805406467115, -0.85181312090299],
      // montrevault sur evre
      [47.272614502727144, -1.01515895466963],
      // ancenis
      [47.38176554923781, -1.1719614475411408],
      //carquefou
      [47.30313303129809, -1.473398828008305]
    ];
    var myMap = null;
    // Fonction d'initialisation de la carte
    function initMap() {
        myMap = L.map('map').setView([47, lon], 9);
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

Tu peux choisir de régler selon le régime libéral. Aucune formalité supplémentaire dans ce cas.

Tu peux aussi choisir de régler en Chèques Emploi Service Universels (CESU). Tu es l’employeur et j’interviens en tant que salarié pour des services à la personne à domicile. La déclaration est à faire sur [le site de l’URSSAF](https://www.cesu.urssaf.fr/info/accueil/s-informer-sur-le-cesu/tout-savoir/c-est-quoi-pour-qui.html).
En utilisant le CESU, tu peux bénéficier d’un avantage fiscal pour les dépenses engagées pour l’emploi d’un salarié à domicile.

Tu peux te simplifier les choses en optant pour le CESU+ : tu délègues alors le processus de rémunération (prélevé directement sur ton compte une fois les coordonnées bancaires saisies). Mon bulletin de salaire est généré automatiquement, il n’y a qu’une seule déclaration à faire en fin de mois. Ce service est gratuit et accessible à tous.

Quelques comités d’entreprise, mutuelle, conseil départemental, proposent des CESU pré-financés (maintenant appelés Titres spéciaux de paiement). Je suis toujours salariée dans le cadre du service à la personne à domicile, le processus de déclaration à l’URSSAF est le même. 
