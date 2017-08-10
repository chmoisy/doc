.. _creating-templates:

Créer des modèles de fiches
###########################

Les modèles sont des fiches de métadonnées que vous pouvez utiliser quand vous commencer à décrire une nouvelle ressource. Cettes section décrit comment charger et gérer les modèles.


Création et gestion de modèles
------------------------------

Les modèles sont gérés de la même manière dans le catalogue que les fichers de métadonnées,
mais elles ont une étiquette 'template'- spéciale.
Elles peuvent être créées, mise à jour et supprimée dans la section ̀``Contribuer`̀.

Les fiches de métadonnées peuvent être converties en modèle et vice-versa n'importe quand 
depuis l'éditeur de métadonnées en utilisant le bouton ``sauver comme modèle``.


.. figure:: img/save-as-templates.png

Les modèles peuvent être affectés à des groupes restreints, de telle façon que seuls ces 
groupes peuvent utiliser le modèle dans leur processus de travail (voir: ref:`managing-privileges`).


Chargement des modèles par défaut
---------------------------------

La page ``Métadonnées et Modèmes`` dans la page d'administration permet de voir 
les standards disponibles.

.. figure:: ../../maintainer-guide/installing/img/metadata-and-templates.png

Depuis cette pages, les utilisateurs peuvent pour chaque standard:

- charger des échantillons par défaut
- charger des modèles par défaut

... s'il y en a de fourni par le plugin du schéma.


Vous devez être connecté comme administrateur pour avoir accès à cette page et à cette fonction.

.. figure:: ../../maintainer-guide/installing/img/templates.png

Import de modèles
-----------------

Une autre façon de charger des modèles est d'utiliser la page d'import de
métadonnées où des fichiers XML peuvent être importés et de sélectionner
le type de fiche: ``modèle``.


.. figure:: img/import-template.png

Création de vos propres modèles
-------------------------------

Chaque standard fournit des échantillons par défaut mais vous devriez penser
à passer du temps à construire votre propre modèle afin de rendre la tâche 
d'édition aussi facile que possible en fonction de : 
- du type de ressources à décrire (par ex : modèles pour des cartes papier)
- de la structure de votre organisation (par ex : définition de modèles par services)
- du type d'utilisation des métadonnées (par ex : utilisation publique, interne, qualité des données)
- du type d'utilisateurs
- ...

Dans un modèle, vous devriez : 
- définir autant de valeurs par défaut que vous le pouvez (par ex : définir le contact par défaut)
- créer les élèments que votre guide de rédaction recommande (pour ne pas perdre de temps à rechercher 
les élèments dans la vue avancée)
- fournir des instructions

Le but principal est de guider le travail de l'éditeur sans avoir besoin de trop de connaissance sur
l'utilisation du standard.

Pour une personnalisation plus poussée, vous pouvez améliorer le plugin du schéma en définissant 
une documentation personnalisée, des valeurs recommandées, etc. (voir :ref:`implementing-a-schema-plugin`)
ou en créant une vue personnalisée (voir :ref:`creating-custom-editor`).
