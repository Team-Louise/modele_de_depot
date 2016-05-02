# Duplicate Content et balise canonique

## Qu'est ce que le Duplicate Content ?

C'est lorsque l'on retrouve le même contenu sur 2 ou plusieurs pages web, que ce soit sur un même site ou sur plusieurs sites différents.
Autrement dit, le cas de multiBàO : on peut retrouver une même fiche sur multibao.org, mais aussi sur tous les sites qui ont intégré la fiche.
Cela pose problème pour l'indexation dans les moteurs de recherche. En effet, ces derniers considèrent le Duplicate Content comme une erreur ou du plagiat. Cela peut entraîner une rétrogradation des pages web dans les résultats de recherche, voire une disparition totale.

## Balise canonique

Pour éviter cela, il existe une balise à intégrer dans le code source des pages web. Elle permet d'indiquer aux moteurs de recherche : "Parmi toutes ces pages dont le contenu est très similaire, merci de ne prendre en compte dans les résultats de recherche que cette URL canonique".
Au départ créée pour gérer les contenus similaires au sein d'un même site web, elle fonctionne depuis 2009 pour des sites différents.

Cette balise est la suivante, à intégrer entre les balises <head> des codes sources de la page canonique et des pages similaires :

< link rel="canonical" href="URL de la page canonique" />

#### Exemple :

Une fiche multiBàO, "L'accélérateur de projet", est présente sur multiBàO, mais aussi sur le blog de M. Patate et sur le site de Mme Courgette.
Il va donc falloir choisir quelle page on considère comme URL canonique (qui apparaîtra dans les moteurs de recherche) :
* http://www.multibao.org/contributions/public/accelerateur_de_projet.md
* http://www.blog-m-patate.fr/accelerateur_de_projet 
* http://www.site-mme-courgette.fr/accelerateur_de_projet --> je choisis cette page comme URL canonique

Puis on intégrera, entre les balises <head> des codes sources de ces 3 pages, cette balise :
< link rel="canonical" href="http://www.site-mme-courgette.fr/accelerateur_de_projet" />

**IMPORTANT : Noter l'URL absolue, c'est-à-dire avec "http://www.".**

## Problèmes et questions

* On ne peut choisir qu'une seule URL canonique, donc si plusieurs sites ont intégré la fiche ça ne sera pas possible de tous les prioriser dans l'indexation des moteurs de recherche. Si on met plusieurs balises, Google décide de n'en reconnaître aucune.
* Semble compliqué à expliquer aux contributeurs s'ils n'ont pas du tout de connaissances en code HTML, car la balise est à mettre dans le code source des pages.
* Où trouver le code source des pages hébergées sur GitHub pour y rajouter la balise ?
* A savoir: la plupart des explications de balise canonique trouvées sur le web correspondent au fonctionnement de Google. Pour les autres moteurs de recherche il est dit que ça peut fonctionner de manière légèrement différente...
