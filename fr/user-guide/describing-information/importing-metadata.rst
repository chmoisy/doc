.. _importing-metadata:

Importer de nouvelles fiches
############################

Un éditeur peu importer des métadonnées dans le fichier catalogue sous différents formats : XML, MEF ou ZIP (voir :ref:`mef_format`).

.. index:: pair: MEF; import
.. index:: pair: XML; import

L'utilisateur doir avoir un profil ``éditeur`` pour pouvoir y accèder. 
Après connexion, aller à la page `̀ contribuer`` et sélectionner le bouton ``Importer 
de nouvelles fiches``

.. figure:: img/import-record-button.png

La page Importer de nouvelles fiches permet d'importer de fiches de trois façons:

* choisir ``Déposer un fichier depuis votre ordinateur`` et choisir un fichier XML ou MEF pour charger les fiches
* choisir ``Copier/coller`` et copier le document XML dans la zone de texte
* Choisir ``Import un ensemble de fichier depuis un dossier du serveur`` et remplir le chemin du dossier


Pour importer plusieurs fichiers en même temps, utiliser le format MEF ou l'option importer du serveur.
Après avoir définit le type d'import, configurez les autres paramètres d'import :

.. figure:: img/import-form.png

- ``Type de fichier``: lors du dépôt ou de la sélection du fichier du serveur, définir le type de fichier à charger. 
   Ce peut être XML pour importer un document XML ou MEF (équivalent à ZIP) pour importer le format MEF.

- ``Type of ficher``:

 - ``Metadonnée`` lors du chargement d'une fiche de métadonnées normale
 - ``Modèle`` lorsque la fiche chargée sera utilisée comme modèle


- ``Traitement de l'identifiant de la fiche`` détermine comment gérer les conflits potentiels entre les UUID des fiches chargées et celles des fiches déjà présentes dans le catalogue. Trois stratégies sont disponibles : 

 - ``Aucun``: l'UUID de la fiche chargée est laissée inchangée. Si une fiche avec le même UUID est déjà présente dans le catalogue, un message d'erreur est renvoyé.

 - ``Ecraser des métadonnées avec le même UUID``: toute fiche existante dans le catalogue avec le même UUID que la fiche chargée sera mise à jour

 - ``Génerer un UUID pour les métadonnées insérées``: un nouvel UUID est assigné à la fiche chargée


- ``Appliquer une conversion XSLT `` permet de transformer la fiche chargée en utilisant un feuille de style XSLT.
  Une liste de transformations prédéfinies est fournie. La transformation sélectionnée doit être compatible avec le
  standard de la fiche chargée (voir :ref:`customizing-xslt-conversion`).


- ``Valider`` déclenche la validation de la ficher avant de la charger. Dans le cas où une erreur survient, la fiche 
  est rejétée et une erreur est renvoyée.

- ``Affecter au catalogue actuel`` affecte la catalogue actuel comme origine de la fiche, dans le cas ou le fichier MEF
  indiquerait une autre source

- ``Affecter au Groupe`` définit le groupe de la fiche chargée.

- ``Affecter à la Categorie`` définit une catégorie locale pour l'affectation de la fiche chargée

Cliquer sur ``importer`` pour déclencher l'import. Après traitement, un résumé est fourni avec les détails suivants:
Click ``import`` to trigger the import. After processing, a summary is provided with

- le nombre total de fiches importées 
- les messages d'erreur
- si seule une fiche est importée, un lien vers cette fiche est fournie
