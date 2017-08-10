.. _linking-online-resources:

Lier des sites, services web, etc. en utilisant une URL
#######################################################

Cette section s'applique principalement aux fiches ISO19139 et partiellement 
aux standards Dublin Core (seuls des documents peuvent être associés dans Dublin Core)

.. _linking-online-resources-doc:

Lier un document
----------------

Deux approches peuvent être utilisées pour lier des documents :
- en fournissant une URL

- en déposant un document

Pour ajouter un nouveau document, cliquez sur le bouton d'ajout + puis sur le bouton
"Ajouter une ressource en ligne" ou, si une existe déjà, cliquez juste sur le titre 
des "Ressource en ligne"


.. figure:: img/addonlinesrc.png

Pour lier une URL, remplir les propriétés suivantes:

- ``Protocole`` pour décrire le type de document attaché  (``adresse web (URL)`` par défaut)
- ``Lien`` pour pointer sur le document cible. Cela peut être n'importe quel type de lien comme http://, ftp://, file:///, ...
- ``Nom`` est optionnel et fournit une étiquette pour la création d'un hyperlien
- ``Description`` est optionnel et fournit plus de détails sur le lien


Pour déposer un document, basculer vers l'ongle "Téléversement" et choisir un document ou glissez/déposez le dans la fenêtre pop-up. Dans ce cas, le protocole est caché et est mis à "WWW:DOWNLOAD"


.. figure:: img/addonlinesrcup.png


Selon vos besoins, des liens plus spécifiques peuvent être ajoutées 
et seront associés à différents actions et affichages dans l'application.


.. _linking-wms-layer:

Lier une couche WMS
-------------------

Afin de pouvoir visualiser une fiche dans le visualiseur de carte, il est 
pertinent d'ajouter une référence à un ou plusieurs services WMS publiant
le jeu de données. Une ressource en ligne est codée en utilisant ce qui suit
en ISO19139:


.. code-block:: xml

     <gmd:onLine xmlns:gmd="http://www.isotc211.org/2005/gmd"
                 xmlns:gco="http://www.isotc211.org/2005/gco">
        <gmd:CI_OnlineResource>
           <gmd:linkage>
              <gmd:URL>https://download.data.grandlyon.com/wms/grandlyon</gmd:URL>
           </gmd:linkage>
           <gmd:protocol>
              <gco:CharacterString>OGC:WMS</gco:CharacterString>
           </gmd:protocol>
           <gmd:name>
              <gco:CharacterString>cad_cadastre.cadsubdivisionsection</gco:CharacterString>
           </gmd:name>
           <gmd:description>
              <gco:CharacterString>Subdivision de section cadastrale (Plan cadastral informatisé du Grand Lyon)(OGC:WMS)</gco:CharacterString>
           </gmd:description>
        </gmd:CI_OnlineResource>
     </gmd:onLine>



Pour ajouter une couche WMS:
- choisir le protocle ``OGC:WMS Web Map Service``,
- remplir l'URL du service,
- puis l'assistant de requête du service pour récupérer la liste de couches
- choisir une ou plusieurs couches de la liste ou remplir le champ manuellement



.. figure:: img/addonlinesrcwms.png


.. _linking-online-resources-georesource:


Lier une table de base données ou un fichier SIG sur le réseau
--------------------------------------------------------------

Pour référencer un fichier SIG ou une table de base de données, l'utilisateur peut déposer 
un fichier ou créer un lien vers cette ressource (voir :ref:`linking-online-resources-doc`). 
Le type de protcole dépend du type de ressource associée:


===================== ==============================================================================================================================================
Type de ressource     Fichier vectoriel déposé (ex :fichier Shapefile zippé)
===================== ==============================================================================================================================================
URL                   URL du fichier créée après dépôt sur le catalogue. ex: http://localhost:8080/geonetwork/srv/eng/resources.get?id=1631&fname=CCM.zip&access=private
Protocole             WWW:DOWNLOAD
Nom                   Nom du fichier (lecture seule)
===================== ==============================================================================================================================================

===================== ==============================================================================================================================================
Type de ressource      Fichier vectoriel sur le réseau
===================== ==============================================================================================================================================
URL                   Chemin de fichier, ex: file:///shared/geodata/world/hydrology/rivers.shp
Protocole             FILE:GEO ou FILE:RASTER
Nom                   Description du fichier
===================== ==============================================================================================================================================

===================== ==============================================================================================================================================
Type de ressource     Vecteur (Table PostGIS)
===================== ==============================================================================================================================================
URL                   jdbc:postgresql://serveur:port/login:password@db
Protocole             DB:POSTGIS
Nom                   Nom de la table
===================== ==============================================================================================================================================


Quand vous disposez des informations sur la base de données ou du fichier sur le 
réseau, il est pertinent de cacher ces informations aux utilisateurs publiques
(voir :ref:`restricting-information-to-metadata-sections`).


.. todo:: Add doc & link to geopublisher



