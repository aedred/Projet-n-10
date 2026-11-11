## Rapport n° 2 — 10/11/2026 au 11/11/2026

### 1. Première impression de la coque du bateau et correction des erreurs

Durant cette séance, j'ai imprimé une première version miniaturisée de la coque de notre catamaran pour avoir un aperçu concret de la version finale.

<p align="center">
  <img width="400" alt="greenboat_miniature_V1_vue_de_biais" src="https://github.com/user-attachments/assets/124cd39a-8d3c-4367-9a09-19a350731f77" />
  <br>
  <em>Figure 1 : Première version miniaturisée de la coque du bateau (vue de biais)</em>
</p>

Cette première impression m'a permis de mettre en évidence une erreur de conception. Initialement, la modélisation prévoyait un perçage à l'arrière pour fixer la barre maintenant le sac de récupération. Le problème, c'est que cette configuration n'utilisait pas la surface utile sous le bateau, là où l'eau et les déchets passent dans tous les cas, entraînant un gâchis d'espace de stockage. J'ai donc redessiné la pièce en ramenant le système de fixation à l'avant.

<p align="center">
  <img width="400" alt="greenboat_miniature_V1_vue_du_haut" src="https://github.com/user-attachments/assets/6e3b7dec-768b-483b-9c53-5ce02c081768" />
  <br>
  <em>Figure 2 : Première version miniaturisée de la coque du bateau vue du haut avec perçage de fixation à l'arrière</em>
</p>

<p align="center">
  <img width="400" alt="greenboat_modélisation_V2_vue_du_haut" src="https://github.com/user-attachments/assets/eebcb117-f9c8-4c60-9286-ded113363c60" />
  <br>
  <em>Figure 3 : Deuxième modélisation de la coque du bateau vue du haut avec perçage de fixation à l'avant</em>
</p>

---

### 2. Prise en main de la carte Raspberry Pi

Pour débuter le projet, nous utilisons une carte Raspberry Pi 3 sans module (le bateau final sera équipé d'un modèle Raspberry Pi 5). 

Pour configurer la carte, j'ai télécharger l'OS Raspberry Pi sur une carte SD avant de l'insérer. J'ai ensuite dû remplacer l'écran d'origine qui dysfonctionnait. Une fois l'affichage opérationnel, j'ai pu configurer correctement le système.

<p align="center">
  <img width="400" alt="Raspberry_demarrage" src="https://github.com/user-attachments/assets/d4faae0e-58ee-4554-9df4-30addcf9ea97" />
  <br>
  <em>Figure 4 : Démarrage et initialisation de la Raspberry Pi</em>
</p>

---

### 3. Intégration de la caméra et détection de bouteilles

J'ai voulu piloter la Raspberry Pi 3 à distance depuis mon ordinateur. La connexion Wi-Fi fonctionnait bien, mais VS Code plantait régulièrement, je suis donc passé par l'invite de commande, beaucoup plus stable. Après avoir branché la caméra qui m'a été prêté pour les tests, la carte l'a reconnue comme une webcam USB standard, ce qui m'a permis d'afficher le flux vidéo sur mon PC via VLC.

J'ai ensuite installé OpenCV et testé avec succès la détection de visages.

<p align="center">
  <img width="400" alt="montage_caméra_vue_du_haut" src="https://github.com/user-attachments/assets/53c3846f-be35-4bb3-9d41-11fc294aff9f" />
  <br>
  <em>Figure 5 : Montage de la caméra sur la Raspberry Pi 3 avec retour vidéo VLC</em>
</p>


La détection de bouteilles s'est avérée plus complexe : un message d'erreur bloquait parfois l'accès à la webcam. Après un redémarrage, le test a fini par identifier correctement la bouteille, mais le programme principal peinait à la repérer de manière fiable — probablement à cause de la faible résolution ou d'un modèle trop léger.

<p align="center">
  <img width="400" alt="détection_de_bouteille" src="https://github.com/user-attachments/assets/8577ebed-bc8e-481b-ac75-d2b57d28766e" />
  <br>
  <em>Figure 6 : Test de détection de bouteille</em>
</p>

### Bilan

La carte Raspberry Pi 3 montre ses limites en termes de puissance de calcul pour cette tâche. La Raspberry Pi 5 couplé à YOLO et à son module améliorera la vitesse et la précision de la reconnaissance des bouteilles. Je pourrai ainsi réutiliser le code d'affichage des données (position, distance, couleur) développé avec l'aide partielle de l'IA.
