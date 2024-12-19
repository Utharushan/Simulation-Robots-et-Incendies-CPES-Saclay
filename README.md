# Projet 2 LIPPS : **Simulation Robots et Incendies**

## Description

Ce projet propose une simulation interactive de gestion d'incendies et de robots pompiers. L'utilisateur peut :
- Charger des **fichiers d'instructions** prédéfinis pour automatiser les actions des robots.
- Créer et utiliser ses propres fichiers d'instructions.
- Jouer en mode interactif pour diriger manuellement les robots à chaque tour.

L'interface graphique, développée avec **Python**, offre une expérience immersive et conviviale pour explorer les dynamiques de propagation du feu et les stratégies d'extinction.

---

## Prérequis

Avant de commencer, assurez-vous que les éléments suivants sont installés :
- **Python** (téléchargez-le [ici](https://www.python.org/downloads/)).
- Bibliothèques Python requises :
  ```bash
  pip install pygame tkinter
  ```

---

## Installation

1. Téléchargez le projet sous forme de fichier ZIP depuis le dépôt "Projet 2 LIPPS".
2. Extrayez les fichiers dans un répertoire de votre choix.
3. Vérifiez que les bibliothèques nécessaires sont installées.
4. Lancez le fichier **`mainInterface.py`** pour démarrer l'application.

---

## Fonctionnalités

### Modes de Jeu

1. **Suivre un Scénario Prédéfini**  
   - Utilise un fichier d'instructions (format : `instructions_nomDeLaCarte`).
   - Chaque fichier contient une série d'actions pour les robots (déplacement, largage d'eau, remplissage).
   - Exemple d'instructions :  
     ```txt
     DRONE,O,O,O,S,S,S,L,E,E,E,R,S,O,O,L,O,L,N,E,L
     ```
     Chaque ligne décrit les actions à effectuer pour un robot spécifique.

2. **Jeu avec le Vent**  
   - Simule la propagation du feu influencée par le vent.
   - Le niveau de difficulté (1 à 3) affecte la probabilité de propagation. Modifiez ce paramètre dans la fonction `lancer_jeu_vent` :
     ```python
     a = jeux_avec_vent(self.sous_menu.options[choix], 1)  # Niveau 1 par défaut
     ```
   - Une boussole est disponible en appuyant sur **B**.

3. **Jeu Solo**  
   - Permet à l'utilisateur de diriger manuellement les robots.
   - Les actions incluent :
     - Choix des directions (N, S, E, O).
     - Largage ou remplissage d'eau.
     - Affichage des attributs et contrôle des robots.

### Contrôles Clavier
| Touche | Action |
|-------|--------|
| **1, 2, 3, etc.** | Sélectionner un robot. |
| **Z, Q, S, D** | Assigner une direction (Nord, Ouest, Sud, Est). |
| **Bas** | Exécuter les actions avec `next()`. |
| **Haut** | Réinitialiser la simulation avec `restart()`. |
| **Gauche** | Larguer de l'eau. |
| **Droite** | Remplir le réservoir. |
| **A** | Afficher les attributs du robot sélectionné. |
| **R** | Voir le niveau d'eau du robot. |
| **M** | Retourner au menu principal. |
| **V** | Contrôler la musique (volume, piste, pause). |
| **H** | Afficher une fenêtre d'aide avec les commandes disponibles. |

---

## Organisation des Fichiers

- **`main.py`** : Point d'entrée principal pour lancer le programme.
- **`Robots.py`** : Implémente les classes et fonctions liées aux robots.
- **`incendie__carte_case.py`** : Gestion des incendies, cartes et cases.
- **`instructions/`** : Répertoire contenant les fichiers d'instructions prédéfinis.
- **`images/`** : Images nécessaires pour l'interface graphique.
- **`README.md`** : Documentation du projet.

---

## Navigation dans le Menu

1. **Modes de jeu** :
   - Utilisez les flèches haut et bas pour sélectionner un mode.
   - Validez avec **Entrée**.

2. **Cartes disponibles** :
   - Choisissez une carte après avoir sélectionné un mode.
   - Navigation et validation identiques.

---

## Auteurs

- **JOLY Tristan**  
  [tristan.joly@universite-paris-saclay.fr](mailto:tristan.joly@universite-paris-saclay.fr)  
- **UTHAYAKUMAR Tharushan**  
  [tharushan.uthayakumar@universite-paris-saclay.fr](mailto:tharushan.uthayakumar@universite-paris-saclay.fr)  

---

## Support

Pour toute question ou suggestion, contactez les auteurs via les emails ci-dessus.  
Découvrez également un **easter egg** caché dans le menu principal !
