## Rapport n°2
  J'ai continué de faire le schéma du circuit électronique du robot, nous devrons le joindre au rapport final et cela nous fera gagner du temps quant au branchement des différents composants lorsque nous les auront tous reçus.
  Je ne l'ai pas encore fini, cependant cela m'a permis de détecter plusieurs erreurs ou oublis critiques: En effet j'ai appris que seul un des ESC devrait être branché sur la broche d'alimentation 5V de la carte Arduino dans le cas où l'on souhaite alimenter celle-ci avec. Brancher le second ESC sur cette même alimentation aurait créé une surchauffe du système qui se serait alors détruit.
  Je suis donc parti du principe que la carte Arduino serait alimentée par l'un des ESC et le câble 5V du second serait isolé du reste du circuit.

  C'est alors qu'un second problème s'est présenté: La carte Raspberry étant connectée par USB à la carte Arduino assurer leur communication, elle alimentait également cette dernière. Nous avions donc deux source d'alimentation vers la carte Arduino, ce qui 
