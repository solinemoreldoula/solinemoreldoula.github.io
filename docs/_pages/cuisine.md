---
layout: single
permalink: /cuisine
title: "Cuisine et pâtisserie à domicile"
---

<div class="image-texte odd">
    <div class="image">
        <img src="/assets/images/cuisine/4.jpg"/>
    </div>
    <div class="texte">
        <div>
            <p>
                Après une naissance, le corps de la femme a besoin de récupérer. L’alimentation y joue un rôle primordial, mais il peut être compliqué de trouver le temps et l’énergie d’anticiper et préparer autre chose que des pâtes au beurre…
            </p>
            <p>
                Forte de mon expérience en pâtisserie et traiteur, je te propose mes services pour te cuisiner des repas chauds et réconfortants.
            </p>  
        </div>
    </div>
</div>

<div class="image-texte">
    <div class="image">
        <img src="/assets/images/cuisine/2.jpg"/>
    </div>
    <div class="texte">
    <div>
    <p>
        A partir d’une liste de menus, tu choisis selon tes goûts et tes habitudes alimentaires. Tu fournis les ingrédients ou je m’occupe des courses (avec un supplément). J’interviens à ton domicile pendant environ 3 heures. </p><p>

A mon départ, tu as une cuisine propre et rangée, des plats tous prêts à consommer (ou à congeler) et une charge mentale allégée.</p></div>
    </div>
</div>

<div class="image-texte odd">
    <div class="image">
        <img src="/assets/images/cuisine/5.jpg"/>
    </div>
    <div class="texte">
    <div>
    <p>
    <b>Forfait 3H</b><br/>
Environ 20 portions (selon les plats choisis) et 10 collations</p><p>

<b>Prix: </b>100 € / 123 € libéral <br/><a  href="#en-pratique-la-différence-entre-le-paiement-en-cesu-et-en-libéral-">Pourquoi 2 tarifs différents ?</a>


</p></div>
    </div>
</div>

## Pour le règlement ?


Paiement possible : 
<ul>
    <li> en libéral (chèques, virement bancaire) </li>
    <li> en CESU (classique ou préfinancé)</li>
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

Tu peux choisir de régler selon le régime libéral. Aucune formalité supplémentaire dans ce cas. Le tarif libéral est plus élevé car il est sujet à des cotisations supplémentaires.


Tu peux aussi choisir de régler en Chèques Emploi Service Universels (CESU). Tu es l’employeur et j’interviens en tant que salariée pour des services à la personne à domicile. La déclaration est à faire sur [le site de l’URSSAF](https://www.cesu.urssaf.fr/info/accueil/s-informer-sur-le-cesu/tout-savoir/c-est-quoi-pour-qui.html).
En utilisant le CESU, tu peux bénéficier d’un avantage fiscal pour les dépenses engagées pour l’emploi d’un salarié à domicile.

Tu peux te simplifier les choses en optant pour le CESU+ : tu délègues alors le processus de rémunération (prélevé directement sur ton compte une fois les coordonnées bancaires saisies). Mon bulletin de salaire est généré automatiquement, il n’y a qu’une seule déclaration à faire en fin de mois. Ce service est gratuit et accessible à tous.

Quelques comités d’entreprise, mutuelles, conseils départementaux, proposent des CESU pré-financés (maintenant appelés Titres spéciaux de paiement). Je suis toujours salariée dans le cadre du service à la personne à domicile, le processus de déclaration à l’URSSAF est le même. 
