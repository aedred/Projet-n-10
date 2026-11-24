## Rapport n°4

  Jeudi dernier, le 19/11/2026, je suis allé à l'intervention du concours Jeunes Pousses concernant le business plan de notre projet: il nous servira entre autres à mieux définir à qui est destiné le produit, s'il sera sujet à la concurrence et de quel manière nous comptons le financer. Il faudra le monter avant le 4 décembre.

# Obtention du GPS et de la carte Arduino

  Nous avons reçu la carte Arduino MEGA ainsi que le GPS, j'ai cherché et trouvé la datasheet de ce dernier ainsi nous l'avons branché et j'ai codé la carte Arduino pour qu'elle renvoie l'orientation, le nombre de satellites perçus par la carte, la longitude, la latitude et la vitesse approximative de la carte.

<img width="4000" height="1848" alt="image" src="https://github.com/user-attachments/assets/4213a03a-261c-459a-ba42-e634a23ba0c5" />

<p align="center">Branchement Arduino et GPS</p>

  Après quelques complications, défauts de bibliothèques et de calibrage, nous avons finalement réussi à lancer le code.

<img width="1612" height="1021" alt="639311405832712696" src="https://github.com/user-attachments/assets/6eb7c2a4-137a-4ae9-a2b5-a29f2d4f1b05" />

<p align="center">Retour des données captées par le GPS</p>

# Montage du circuit à deux moteurs

  Par la suite nous avons recréé le montage de la semaine dernière en y ajoutant le second moteur. En conséquence nous avons utilisé des connecteurs afin de brancher en parallèle les ESC et les moteurs.

<img width="1865" height="1636" alt="20261124_171936v" src="https://github.com/user-attachments/assets/cfd5233f-76e7-4c89-8992-44a9f6ed18c9" />

<p align="center">Montage à deux moteurs</p>

  Nous avons rencontré quelques difficultés pour relier les câbles, plus épais, en provenance de l'alimentation aux connecteurs mais nous finalement réussi à alimenter tout le circuit.
  On peut cependant noter un tressautement répété d'une dizaine de secondes au niveau de l'un des moteurs lorsque l'on éteint le montage, nous ne savons pas encore à quoi il est dû mais cela ne devrait pas poser de problèmes en définitive.
