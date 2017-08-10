.. _linking-parent:

Regrouper des jeux de données dans une série (ie. relation parent/enfant)
#########################################################################

Dans certains cas, un jeu de données est une partie d'une collection temporelle 
ou spatiale de fiches qui peuvent partager les mêmes spécificités (par ex : occupation
du sol pour plusieurs années). Pour regrouper cette ensemble de fiches, une 
description générale de la collection peut être faire dans les métadonnées 
d'un parent qui est alors lié à chaque jeux de données de la série.


- Corine Land Cover

 - Corine Land Cover 2002
 - Corine Land Cover 2012
 - ...

Les relations parent/enfant peuvent être remplies dans les fiches ISO19139 et Dublin
Core. Dans le cas de ISO19139, le lien vers une fiche parente est codée dans la fiche
enfant de la manière suivante:


.. code-block:: xml

   <gmd:parentIdentifier>
      <gco:CharacterString>78f93047-74f8-4419-ac3d-fc62e4b0477b</gco:CharacterString>
   </gmd:parentIdentifier>

Les relations parent/enfant dans l'ISO19139 peuvent aussi être codées en utilisant des
aggrégats (voir :ref:`linking-others`).

Lors de la création d'une telle relation, les utilisateurs seront capables de naviguer
entre les fiches dans les vues recherche et fiche.

.. todo:: Add screenshot

Cliquer sur ''Lien vers parent'' pour accèder au panneau fournissant une recherche 
simple pour sélection les métadonnées parent cible.


.. figure:: img/parent.png


