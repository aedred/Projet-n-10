## Rapport n°3

# Introduction

  J'ai commencé la séance en cherchant à résoudre les problèmes découvert à la dernière.

# Solution apportée au problème d'alimentation de la carte Raspberry

  Comme dit précédemment j'ai cherché un convertisseur buck step/down susceptible de convenir pour transformer la tension 12V des batteries en 5V fournis à la carte Raspberry.
  J'en ai trouvé un sur Amazon, fonctionnant à 5A (soit l'intensité nominale de la carte Raspberry).

<img width="838" height="539" alt="image" src="https://github.com/user-attachments/assets/cd60bd5b-4a47-47bc-9816-3cf1173be967" />

Voici le lien vers le produit:  
https://www.amazon.fr/Hoembpn-Convertisseur-Alimentation-Transformateur-R%C3%A9gulateur/dp/B0FN6JM61V/ref=sr_1_8?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&sr=8-8

# Mise au propre du schéma électrique

  Par la suite j'ai refait le schéma électrique à l'aide du logiciel QElectrotech afin de posséder une version plus présentable de celui-ci. A noter cependant que j'ai crée des blocs simplifiés des différents composants car seule la carte Arduino existait dans la bibliothèque du logiciel.
  Ainsi les composants que j'ai crée sont des blocs ne comprenant que les bornes et leurs noms (pas de dessins détaillés à la manière des modèles natifs du logiciel).

<img width="655" height="747" alt="image" src="https://github.com/user-attachments/assets/11337d27-1371-4338-bbc7-b8b38c355abb" />


<p align="center">Circuit électrique définitif</p>   

# Suite de la séance

  N'ayant pas d'autres tâches à accomplir dans l'immédiat (nous n'avons pas encore reçu nos cartes Arduino et Raspberry, donc aucun montage possible), j'ai brièvement aidé mon binôme au cours de la mise en route d'un montage visant à tester nos moteurs et composé d'une Arduino, un ESC et le moteur brushless.
  Nous avons commis une erreur de manipulation se résultant par la perte de notre alimentation de test, mais sans pertes humaines.
  En-dehors de cet incident les autres tests se déroulèrent correctement.

# Conclusion

  Si le matériel n'est pas arrivé d'ici la semaine prochaine je me mettrais en quête d'une Raspberry ou d'une Arduino de génération moins récente que celle demandée afin
