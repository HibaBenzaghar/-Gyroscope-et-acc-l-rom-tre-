# Projet Gyroscope et Accéléromètre MPU6050
## Introduction  
Ce projet utilise un module MPU6050 (gyroscope + accéléromètre) pour détecter l’orientation et afficher la direction (haut, bas, gauche, droite) et l'accélération sur un écran LCD I2C 16x2. Il permet de mieux comprendre comment lire et interpréter les données d’un capteur inertiel en temps réel, avec un affichage simple.



## Liste des composants

- Arduino Uno  
- Module IMU MPU6050  
- Écran LCD 16x2 avec interface I2C  
- Câbles de connexion (dupont male-male)  
- Breadboard
- Alimentation 5v

## Schéma électronique

<img width="408" alt="image" src="https://github.com/user-attachments/assets/5713927e-edbf-491a-930d-1074d48480c9" />


*Le schéma montre les connexions principales :*  
- SDA (LCD) → A4 (Arduino)  
- SCL (LCD) → A5 (Arduino)  
- VCC (LCD & MPU6050) → 5V Arduino  
- GND (LCD & MPU6050) → GND Arduino  
- MPU6050 connecté en I2C sur SDA/SCL Arduino  

## Explication simple du code

Le code est écrit en Arduino IDE et fait les étapes suivantes :

1. Initialiser la communication I2C avec le module IMU et l’écran LCD.  
2. Calibrer le gyroscope et l’accéléromètre pour minimiser l’erreur.  
3. Lire les données brutes du capteur IMU.  
4. Calculer les angles d’inclinaison (roll, pitch, yaw).  
5. Afficher les valeurs calculées et la direction (haut/bas) sur l’écran LCD.  
6. Envoyer les données au port série pour debug (optionnel).  


## Photos ou captures d’écran
Start:
![WhatsApp Image 2025-06-11 à 15 40 21_0e207a39](https://github.com/user-attachments/assets/9d2e749a-d353-4479-93dd-5cab8e7c77d6)
Working:
![WhatsApp Image 2025-06-11 à 15 40 52_00fe378c](https://github.com/user-attachments/assets/73b5fa34-8397-4766-9c18-858dda9c1cdb)
![WhatsApp Image 2025-06-11 à 15 41 17_761649b7](https://github.com/user-attachments/assets/cc679bfa-6355-4a55-bc95-7ef6c44f8b9a)
![WhatsApp Image 2025-06-11 à 19 03 23_41e3f92c](https://github.com/user-attachments/assets/048a04b7-573b-472b-a7b6-d8bf74f95b42)



## Vidéo de démonstration
https://youtube.com/shorts/durMujPbixI?si=PIUfneER4diqM4VX
https://youtube.com/shorts/durMujPbixI?si=PIUfneER4diqM4VX
https://youtube.com/shorts/d7HRCWKiFtE?si=rqMBNyRJBchXtX6A
https://youtube.com/shorts/WYKy4-q5Adw?si=LnA5E9QnaUxR04ia


## Comment utiliser le projet

1. **Installation du matériel**  
   - Connecter le module IMU aux broches SDA (A4) et SCL (A5) de l’Arduino.  
   - Brancher l’écran LCD I2C sur les mêmes broches SDA/SCL.  
   - Alimenter le circuit en 5V et GND.  

2. **Installation logicielle**  
   - Installer l’IDE Arduino.  
   - Installer les bibliothèques nécessaires : `Wire.h`, `LiquidCrystal_I2C.h`, `MPU6050.h` (ou celle que tu utilises).  
   - Ouvrir le fichier `sketch.ino` (ou `main.ino`).  

3. **Téléversement**  
   - Sélectionner la carte Arduino Uno dans l’IDE.  
   - Connecter la carte en USB.  
   - Compiler et téléverser le code.  

4. **Utilisation**  
   - Allumer l’Arduino, l’écran LCD doit afficher les directions et l'acceleration.  
   - Observer les données qui évoluent lorsqu'on bouges le capteur.  

---

## Remarques

- Pour améliorer la précision, on peut ajouter un filtre complémentaire ou un filtre de Kalman.  
- Ce projet est une base pour intégrer des contrôles de mouvements ou stabilisation.  


*Fait avec ❤️ par notre équipe.*

