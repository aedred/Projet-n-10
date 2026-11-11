Rapport n°2 : 10/11/2026 - 11/11/2026

1 ) Première impression de la coque du bateau et correction des erreurs

Dans cette séance j'ai imprimer, une première version miniaturisé de la coque de notre bateau pour avoir un aperçu de la version finale.

<p align="center">
  <img width="400" alt="greenboat_miniature_V1_vue_de_biais" src="https://github.com/user-attachments/assets/124cd39a-8d3c-4367-9a09-19a350731f77" />
  <br>
  <em>Figure 1 : Première version miniaturisée de la coque du bateau (vue de biais)</em>
</p>

Cette première version m'a permis de me rendre compte d'une erreur de logique dans la modélisation de la coque du bateau (catamaran) en effet notre bateau tel que la modélisation à été faite vient fixer grâce à un percage pour y loger une barre qui tiendra le sac à l'arrière du bateau ce qui fait que toute la surface sous le bateau ou les déchets passent pour rentrer dans le sac n'est pas utiliser pour stocker ce qui est un gachis de place, j'ai donc ramener le système de fixation à l'avant 

<p align="center">
  <img width="400" alt="greenboat_miniature_V1_vue_du_haut" src="https://github.com/user-attachments/assets/6e3b7dec-768b-483b-9c53-5ce02c081768" />
  <br>
  <em>Figure 2 : Première version miniaturisée de la coque du bateau vue du haut avec perçage de fixation à l'arrière </em>
</p>

<p align="center">
  <img width="400" alt="greenboat_modélisation_V2_vue_du_haut" src="https://github.com/user-attachments/assets/eebcb117-f9c8-4c60-9286-ded113363c60" />
  <br>
  <em>Figure 3 : Deuxième modélisation de la coque du bateau vue du haut avec perçage de fixation à l'avant </em>
</p>



2 ) Début de l'utilisation d'une carte Raspberry

Pour le début du projet nous devons utiliser une carte Raspberry PI 3 sans module (celle qui occupera le bateau sera équipé d'une carte Raspberry PI 5)
Pour pouvoir prendre en main cette carte, j'ai du télécharger le logiciel de la Raspberry sur une carte SD pour l'utiliser, je l'ai ensuite mise dans la carte.
J'ai ensuite du trouver démonter l'écran utiliser pour la Raspberry pour le remplacer car il dysfonctionnait, une fois l'écran utilisable j'ai pu configurer la carte pour l'utiliser. 

<p align="center">
  <img width="400" alt="Raspberry_demarrage" src="https://github.com/user-attachments/assets/d4faae0e-58ee-4554-9df4-30addcf9ea97" />
  <br>
  <em>Figure 4 : Raspberry, démarrage et initialisation </em>
</p>



3 ) Prise en main d'une caméra avec la Raspberry 3 pour la détection de bouteilles

J’ai voulu piloter ma Raspberry Pi 3 depuis mon ordinateur. La connexion à distance via le Wifi a bien marché, mais le logiciel VS Code n’arrêtait pas de se bloquer, alors je suis passé par l’invite de commande, plus simple. J’ai branché la caméra, et la carte ne la voyait pas comme une caméra classique, mais l’a bien reconnue comme une caméra USB, et j’ai réussi à voir son image sur mon ordinateur avec VLC.

J’ai ensuite installé OpenCV et testé la détection de visages, qui a bien fonctionné.


<p align="center">
  <img width="400" alt="montage_caméra_vue_du_haut" src="https://github.com/user-attachments/assets/16dabc13-771e-41c5-b8cd-2e7e76c23d0e" />
  <br>
  <em>Figure 5 : Montage de la caméra emprunté à la Raspberry PI 3 avec retour vidéo VLC </em>
</p>



Pour détecter une bouteille, j’ai eu plus de mal : un message d’erreur empêchait parfois d’ouvrir la webcam. Une fois tout réparé après un redémarrage, mon test voyait bien la bouteille, mais le programme principal la ratait souvent, sans que je sache si c’était à cause de l’image trop petite ou d’un modèle trop faible.


<p align="center">
  <img width="400" alt="détection_de_bouteille" src="https://github.com/user-attachments/assets/8577ebed-bc8e-481b-ac75-d2b57d28766e" />
  <br>
  <em>Figure 6 : Teste de détection de la bouteille </em>
</p>



J’en conclus que ma carte Raspberry PI 3 n’était pas assez puissant pour ce travail. Je vais donc passer à un Raspberry Pi 5 avec YOLO, qui devrait mieux reconnaître les bouteilles et le faire plus vite, et je pourrai réutiliser mon code d’affichage des informations (position, distance, couleur) construit à l'aide de l'IA dans un premier temps.
