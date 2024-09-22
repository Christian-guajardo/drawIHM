# Rapport sur le Programme Java

## Auteur et Contributeurs

- le nom des auteurs:

 MEDDOUS Celia, 

 BACAR Houssam,

  Nunez Guajardo Christian-Esteban,

 Da costa Mathieu.


## Rendu
  Partie 1

  - Exercice 1 :
  Ajout des fonction de déplacement et de changement de couleur de robi.

  - Exercice 2 :
  Ajout des fonction de lecture des scripte, et également du sleep pour faire la pause entre deux instruction.

  - Exercice 3:
  Ajoute de l’interface commande avec les premier mot clé utiliser. (space, color, robi, translate).

  - Exercice 4:
  Amélioration du code pour permettre de crée d’autre objet que robi, grâce a des objet de référencer.
  4.2
  Ajoute de la possibilité de crée de nouveaux objet comme : ovale, image, texte. Et également de la suppression de ces élément.

  - Exercice 5:
  Ajoute la possibliter de redimensionner les objet ovale et rect, et de crée d’autre objet a l’intérieur de ces dernier.

Partie 2:

  Basé sur l'exercice 5.

  2 - Ce qu'on a reussi à faire :

1.  ->Convertir un dessin en BufferImage et le convertir en base64.
1.  -> Faire des capture au moment de translation.
1.  -> Mettre en place le package JSON.
1.  -> Faire l'interface graphique en Java Swing.
1.  -> Faire un client/Serveur.
1.  -> faire un objet RobiOject permettant de jouer le rôle D'objet de conversion en JSON.
1.  -> Créer une interface graphique.

 

## défficulté retrouvé: 

1 - L'une des difficultés identifiée est de capturer une image de space après l'éxécution de script coté serveur et de la retourner au client. Cette image doit être encodée en base64 pour être envoyée au client, puis la décodée et l'affichée côté client.

2 - Difficulté sur la prise en main de l'interface graphique Swing : cela demande une bonne organisation du code 

2 - Difficulté lors de la création de thread avec l'interface graphique swing 


## Elements techniques et solutions

Le resultat retourner par le serveur est une image encodée en base64, ca nécessitera la création d'un thread coté qui décode continuellement l'image (base64) en image prete à etre afficher. Autrement dit c'est de faire la construction de l'image coté client à partir de l'image en base64 renvoyé par le serveur.



## Bilan 
On complique les choses à chaque fois on pense loin pour touver une solution aux problèmes alors que la solution est très simple.

Problème:

L'ajout d'un objet graphique dans le space nécessite de créer un environnement. Un environnement globale existe déjà pour le space. Néanmoins dans notre code les Elements graphique sont tous ajoutés à un environnement global, c'est-à-dire le même environnement au lieu d'etre ajoutés à un nouveau environnement(de chaque element). Cela a des consequence sur l'espace de nom des objets. La suppression d'un élément dans un environnement nécessite d'utiliser l'espace de nom se traduisant par des erreurs de suppression au sein d'un même environnement. Au final, un element ajouté portant le même nom écrase un autre portant ce même nom, et la suppression d'un élément écrasé mais existant en tant qu'objet dans la mémoire ne peut être effective. 

Finalement, on aurai du mettre à jour les environnements (de chaque élément crée) en locale dans la fonction addElement et delElement.


## Fonctionnalités non implémentées

1. Exercice 6 de la 1er Partie nom implémentées.

4. Affichage de l'environnement et des SNode.

5. Renvoi de commandes graphiques à la place d'une image.








"# drawIHM" 
