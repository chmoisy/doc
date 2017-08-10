.. _linking-thumbnail:

Illustration avec un aperçu
###########################

Pour aider l'utilisateur à identifier un fiche intéressante, vous pouvez créer
un aperçu graphique (ou vignette) sous la forme d'une image et l'attacher à la
fiche de métadonnées. Par exemple, si votre fiche de métadonnées décrit des jeux
de données géographiques alors l'aperçu graphique pourra être une image de la carte
avec une légende produite pas un service OGC WMS (Web Map Service).

Vous pouvez associer une ou plusieurs vignettes à une fiche.


Les vignettes sont affichées dans les vues de recherche et de métadonnées:

.. figure:: img/thumb-in-search-results.png


Depuis de le panneau ''Ressources associées'', cliquez sur le bouton ''Ajouter une vignette''
pour ouvrir l'assistant "d'ajout d'aperçu à la métadonnée". Les vignettes peuvent être ajoutées
de trois façons : 


Liaison d'une vignette avec une URL
-----------------------------------

Quand la vignette est disponible comme image sur le web, elle peut être liée directement
à la ficher de métadonnées. Ajouter une description facultative pour décrire l'image : 

.. figure:: img/thumb.png

Vous pouvez lier autant d'images que vous le souhaitez. Les images associées dans ce mode
doivent accessibles publiquement sur le web si vous voulez que les vignettes soient affichées
correctement même si les fiches de métadonnées sont récoltées par d'autre catalogues.


Dépôt d'une vignette
--------------------

Seules deux vignettes peuvent être rattachées à une fiche et déposées sur le catalogue.
De manière optionnelle, une petite vignette peut être créée automatiquement lors du 
dépôt d'une grande image.

Les formats d'image suivants sont supportés:

 - GIF,
 - PNG
 - JPEG


Choisissez un fichier sur votre ordinateur ou glissez&déposer un fichier sur la fenêtre
pop-up. Cliquez sur "Ajouter une vignette" pour déclencher le dépôt.


.. _linking-thumbnail-from-wms:


Génération d'une vignette en utilisant des couches WMS
------------------------------------------------------

Si vous avez enregistré une couche WMS dans la fiche de métadonnée actuelle (voir :ref:`linking-wms-layer`),
une vignette peut être générée l'utilisant par dessus la couche cartographique de base.
Sélectionner l'onglet ''créer une vignette" et choisir la zone à imprimer sur la vignette.


.. figure:: img/thumbprint.png




