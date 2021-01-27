# Mask_detection

## Contexte du projet

Avec la pandémie COVID-19, dans pas mal de pays le port de masques est devenu obligatoire pour se protéger contre ce virus mortel. Dans ce projet, vous alllez développer un modèle IA - Détecteur de masque sur les images en premier temps puis en temps réel avec Python.




##Description de l'architecture
les données passent d'abord par une normalisation puis passent trois fois de suite par une couche de Conv2D et une couche de maxpooling. Enfin, nous leur appliquons un Flatten pour les remettre à plat et deux dense (ReLu puis sigmoid) pour récupérer le bon format de sortie (un booléen 0 ou 1).
Puis au moment de le compiler nous avons utilisé la 'binary_crossentropy' qui a en général de meilleurs résultats lorsque les prédictions sont binaires.


##Conclusion
Nous avons testé deux réseaux différents (bien qu'assez similaires) l'un utilisant des activations de type 'reLu', et l'autres sans activations. Les résultats sur la matrice de confusion allaient clairement en faveur du modèle 'reLu', c'est donc celui que nous avons choisi de conserver.
Nous avons quand même réalisé que notre modèle manquait d'entraînement (la base de données d'images était trop petite et pas assez diversifiée) et par conséquent les résultats sont mitigés. Le modèle ne détecte correctement que les visages correctement illuminés (ni trop ni trop peu), bien cadrés et proches de la caméra. Nous avons également pu constater qu'en plaçant des visages à un endroit précis de l'écran, il pouvait détecter la présence d'un masque même s'il n'y en avait pas.
Notre modèle est probablement correct, mais ses résultats seraient optimisés avec une base d'apprentissage plus grande.
