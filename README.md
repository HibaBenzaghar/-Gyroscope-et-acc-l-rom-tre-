# Projet Gyroscope et Accéléromètre MPU6050
## Introduction  
Ce projet utilise un module MPU6050 (gyroscope + accéléromètre) pour détecter l’orientation et afficher la direction (haut, bas, gauche, droite) et l'accélération sur un écran LCD I2C 16x2. Il permet de mieux comprendre comment lire et interpréter les données d’un capteur inertiel en temps réel, avec un affichage simple.


## Liste des composants  
- Arduino Uno R3  
- Module MPU6050 (Gyroscope + Accéléromètre)  
- Écran LCD I2C 16x2  
- Câbles de connexion (jumpers)  
- Breadboard (optionnel)  


## Schéma électronique  
<img width="434" alt="image" src="https://github.com/user-attachments/assets/89762c63-e946-41b3-90c3-1d93b491aa56" />



## Explication du code  
1. Initialisation du MPU6050 et calibration des capteurs pour corriger les erreurs de base.  
2. Lecture des valeurs brutes de l’accéléromètre et du gyroscope.  
3. Calcul des angles d’orientation (roll, pitch, yaw) à partir des données brutes.  
4. Détection de la direction en fonction de l’angle (par exemple : inclinaison vers le haut ou vers le bas).  
5. Affichage de la direction détectée sur l’écran LCD en temps réel.


## Photos / Captures d’écran  


## Vidéo de démonstration  


## Comment utiliser le projet  

### Câblage  
- **MPU6050**  
  - VCC → 5V  
  - GND → GND  
  - SDA → A4 (Arduino Uno)  
  - SCL → A5 (Arduino Uno)  
- **LCD I2C 16x2**  
  - VCC → 5V  
  - GND → GND  
  - SDA → A4  
  - SCL → A5  

### Installation et téléversement du code  
1. Ouvrir le fichier `sketch.ino` dans l’IDE Arduino.  
2. Sélectionner la carte **Arduino Uno** dans le menu **Outils > Type de carte**.  
3. Choisir le port COM correspondant à la carte.  
4. Cliquer sur **Téléverser**.  

## Remarques  
- les bibliothèques Arduino pour MPU6050 et LCD I2C sont bien installées (ex : `Wire.h`, `LiquidCrystal_I2C.h`, `MPU6050.h`).  
- Ce projet peut être amélioré en ajoutant la gestion d’autres mouvements, ou en optimisant la calibration.  
 
