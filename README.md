# Independent-sets


## Feuille de route
Etant donné un corpus, l’objectif est de décrire chaque document par un ensemble de termes diversifiés ayant de fortes
valeurs TF-IDF.

Chaque document est prétraité pour détecter des termes (mots ou groupes de mots) 1 . On sélectionne les termes ayant
une valeur supérieure à un seuil fixé (paramètre du programme). On crée un graphe de similarité G entre ces termes. On
calcule ensuite plusieurs maximal independent sets de G comprenant le terme t ayant le score TF-IDF le plus élevé 2 .

Parmi les maximal independent sets ainsi créés, on identifie celui dont la somme des poids (les poids des sommets sont
ici les valeurs TF-IDF des termes) est maximale. Un programme est ensuite créé qui permet pour un document donné
(passé comme argument) d’afficher son graphe G avec les sommets appartenant au meilleur independent set en rouge et
les autres en bleu.

Les données à utiliser sont NG20 facilement accessible par Scikit, et Classic3 disponible à l’adresse :
https://mycloud.mi.parisdescartes.fr/s/HwpG4bmaRp3sSCC
