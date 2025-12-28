# 🚀 Projet Apollon

Le **Projet Apollon** est un ordinateur de vol open-source haute performance conçu pour les fusées amateurs. Il repose sur une architecture distribuée de quatre contrôleurs communiquant via un réseau P2P, offrant une puissance de calcul et une redondance exceptionnelles pour la navigation et l'analyse de données en temps réel.

## 🏗️ Architecture du Système

Le cœur d'Apollon est divisé en quatre unités spécialisées pour garantir une latence minimale et une fiabilité maximale :

| Module | Microcontrôleur | Rôle Principal |
| --- | --- | --- |
| **TLM** (Télémesure) | ESP32-S3 | Liaison LoRa, Point d'accès WiFi/Bluetooth, interface station sol. |
| **NAV** (Navigation) | STM32H723ZGT6 | Fusion de capteurs (GPS, Météo, IMU), enregistrement des données (Blackbox). |
| **ML** (Machine Learning) | STM32H743ZIT6 | Prédiction de trajectoire et raffinement de modèle IA en temps réel. |
| **MCU** (Main Control Unit) | STM32G474CET3 | Maître de la chronologie (séquençage) et gestionnaire du réseau P2P. |

---

## ✨ Caractéristiques Clés

* **Réseau P2P Inter-puces :** Une communication fluide et rapide entre les quatre contrôleurs pour une synchronisation parfaite.
* **Intelligence Embarquée :** Utilisation du Machine Learning pour prédire l'apogée et optimiser la récupération.
* **Connectivité Étendue :** Suivi longue distance via LoRa et configuration facile via une interface Web/App (WiFi/BT).
* **Structure Paramétrique :** Conception mécanique adaptable pour s'intégrer dans différents diamètres de fusées (du 38mm aux gros diamètres) et supporter diverses masses.
* **Open Source :** Conçu par et pour la communauté de l'aérospatial amateur.

---

## 🛠️ Stack Technique

* **Langages :** C/C++ (Embedded), Python (pour l'entraînement des modèles ML), HTML/CSS/Javascrypt/PHP (pour l'interface web), SQLite (pour le stockage des données).
* **Outils :** STM32CubeIDE, ESP-IDF, Antigravity, Autodesk Fusion 360, EasyEDA (pro edition).
* **Communication :** Protocole P2P propriétaire, LoRa, SPI/I2C pour les capteurs internes.
* **Conception Mécanique :** CAO paramétrique (compatible avec les outils comme FreeCAD ou Fusion 360).

---

## 📂 Structure du Dépôt

```text
├── firmware/
│   ├── TLM/              # Code de télémesure et connectivité
│   ├── NAV/              # Traitement des données capteurs
│   ├── ML/               # Modèles d'IA et prédiction
│   └── MCU/              # Gestion centrale et chronologie
├── hardware/             # Schémas PCB et fichiers Gerber
│   ├── TLM/              
│   ├── NAV/             
│   ├── ML/             
│   └── MCU/ 
├── mechanical/           # Fichiers CAO de la structure paramétrique
└── docs/                 # Documentation technique et protocole P2P

```

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Que ce soit pour améliorer les algorithmes de navigation, optimiser les modèles de ML ou tester la structure paramétrique sur de nouveaux châssis.

1. Forkez le projet.
2. Créez votre branche de fonctionnalité (`git checkout -b feature/AmazingFeature`).
3. Commitez vos changements (`git commit -m 'Add some AmazingFeature'`).
4. Poussez vers la branche (`git push origin feature/AmazingFeature`).
5. Ouvrez une Pull Request.

---

## 📜 Licence

Distribué sous la licence MIT. Voir `LICENSE` pour plus d'informations.

---

**Note :** *Ce projet est destiné à un usage éducatif et expérimental. Assurez-vous de respecter la réglementation locale concernant le lancement de fusées amateurs.*

---

Souhaitez-vous que je développe une section plus spécifique, comme les détails du protocole de communication P2P ou la liste des capteurs prévus ?
