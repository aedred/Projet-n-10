## Rapport n°2

# Résumé de séance

  J'ai continué de faire le schéma du circuit électronique du robot, nous devrons le joindre au rapport final et cela nous fera gagner du temps quant au branchement des différents composants lorsque nous les auront tous reçus.
  Je ne l'ai pas encore fini, cependant cela m'a permis de détecter plusieurs erreurs ou oublis critiques.

# Conflit d'alimentation des ESC
  
  En effet j'ai appris que seul un des ESC devrait être branché sur la broche d'alimentation 5V de la carte Arduino dans le cas où l'on souhaite alimenter celle-ci avec. Brancher le second ESC sur cette même alimentation aurait créé une surchauffe du système qui se serait alors détruit.
  Je suis donc parti du principe que la carte Arduino serait alimentée par l'un des ESC et le câble 5V du second serait isolé du reste du circuit.

# Alimentation de la carte Raspberry

  C'est alors qu'un second problème s'est présenté: La carte Raspberry étant connectée par USB à la carte Arduino assurer leur communication, elle alimentait également cette dernière car elle ne peut elle-même être fonctionnelle seulement si elle est alimentée par des batterie (la brancher en USB ne suffit pas). Nous avions donc deux sources d'alimentation vers la carte Arduino, ce qui mène également à l'endommagement du matériel.
  Nous sommes donc contraints de trouver une solution quant à l'alimentation de la carte Raspberry.

 # Solutions envisagées

  A cela, deux réponses se présentent: La première consiste à utiliser la sortie 5V de l'ESC, initialement prévu pour alimenter la carte Arduino, en la branchant sur l'alimentation de notre Raspberry. Ce n'est certainement pas la meilleure solution: Elle a le mérite de résoudre le conflit de double alimentation cependant nous manquerons de puissance pour faire fonctionner la carte Raspberry et le NPU nécessaire à faire fonctionner notre modèle d'I.A., l'ESC ne pouvant fournir que 3A à la carte qui nécessiterait 5A pour être opérationnelle.
  Dans le meilleur des cas on peut espérer que la carte s'éteigne en boucle, et dans le pire celle-ci forcera l'ESC pour obtenir le courant nécessaire, ce qui provoquera une surchauffe et la destruction de celui-ci.

  L'autre solution consiste à brancher la carte Raspberry sur le moniteur de batterie (lui-même branché à la batterie LiPo). Pour cela nous devrons cependant faire le pont entre les deux composants avec un convertisseur Buck (Step/Down) pouvant convertir les 12V délivrés par la batterie en 5V pour éviter une nouvelle fois que la carte ne soit endommagée.

# Aperçu du schéma électrique (non fini, stade de développement)

<img width="807" height="687" alt="image" src="https://github.com/user-attachments/assets/a914f7a3-6695-45a1-a219-426973e12206" />

# Conclusion du rapport

  Je vérifierai l'existence de possibles alternatives s'il en existe mais je pense que la dernière solution reste la seule viable si l'on souhaite avoir la puissance nécessaire au fonctionnement de notre algorithme d'I.A. et l'absence de problème d'alimentation.
