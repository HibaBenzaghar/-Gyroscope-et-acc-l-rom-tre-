# Projet Gyroscope et Accéléromètre MPU6050
## Introduction  
Ce projet utilise un module MPU6050 (gyroscope + accéléromètre) pour détecter l’orientation et afficher la direction (haut, bas, gauche, droite) et l'accélération sur un écran LCD I2C 16x2. Il permet de mieux comprendre comment lire et interpréter les données d’un capteur inertiel en temps réel, avec un affichage simple.


## Matériel utilisé

- Arduino Uno R3  
- Module MPU6050 (Gyroscope + Accéléromètre)  
- Écran LCD 16x2 I2C  
- Câbles de connexion  
- Breadboard


## Étapes réalisées

### 1. Connexion du matériel

On a d’abord connecté le module MPU6050 à l’Arduino via I2C (SDA sur A4, SCL sur A5).  
Ensuite, on a connecté l’écran LCD I2C sur les mêmes broches SDA et SCL, en parallèle.

### 2. Importation des bibliothèques

On a ajouté dans le code Arduino les bibliothèques nécessaires pour communiquer avec le MPU6050 (`Wire.h`, `MPU6050.h`) et pour l’écran LCD (`LiquidCrystal_I2C.h`).

### 3. Calibration

On a écrit une fonction pour calculer l’erreur initiale de l’IMU, appelée `calculate_IMU_error()`, afin de corriger les mesures du gyroscope.

### 4. Lecture des données

Dans la boucle principale, on a récupéré les valeurs de l’accélération et de la rotation, et calculé l’angle d’inclinaison en roll et pitch.

### 5. Affichage

On a affiché la direction détectée sur l’écran LCD. Par exemple, si l’inclinaison dépasse un seuil, on affiche “Haut” ou “Bas” selon l’axe.

### 6. Tests et améliorations

Au début, l’affichage était instable. On a amélioré la gestion des erreurs et ajouté un filtre pour stabiliser la lecture.


## Schéma électronique

Le schéma électronique est disponible dans le dossier `schematic/`.  
Il montre les connexions entre l’Arduino, le MPU6050 et l’écran LCD.


## Code source

Le code complet se trouve dans le dossier `code/`, fichier `sketch.ino`.


## Photos

Des photos du montage sont dans le dossier `photos/`.


## Conclusion

Ce projet nous a permis de mieux comprendre la lecture des capteurs inertiels et l’affichage sur un LCD I2C.  

