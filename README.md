# Cours de Technologie - Robot Pousseur avec Pare-chocs
## Séance de Synthèse - 3ème année Collège

---

## Introduction au Projet

Le projet consiste à concevoir et réaliser un **robot pousseur avec pare-chocs** pour le robot Mbot. Ce système permettra au robot de pousser des jantes dans un circuit sans en sortir.

### Contexte
- **Projet** : Robot pousseur - Conception numérique et impression 3D
- **Langage de modélisation** : SysML (System Modeling Language)
- **Objectif** : Comprendre le fonctionnement du système à travers différents diagrammes

---

## 1. Le Cahier des Charges Fonctionnel (CDCF)

### Fonction Principale (FP)
**FP1** : Permettre au robot de pousser les jantes

### Fonctions Contraintes (FC)

| N° | Fonction / Contraintes | Critère | Niveau d'exigence |
|----|------------------------|---------|-------------------|
| **FP1** | Permettre au robot de pousser les jantes | Vitesse | Le robot ne doit pas être ralenti |
| **FC1** | Être réalisable au collège | Matériel/Matériau/Élèves | Charlyrobot / Imprimante 3D<br>3ème, maîtrise des logiciels Charlygraal/SolidWorks |
| **FC2** | Ne doit pas toucher le sol | Contact | Pas de contact avec le sol |
| **FC3** | S'adapter au châssis du robot Mbot | Liaison/fixation | Sans modification du châssis |
| **FC4** | Adaptation pour plaire l'utilisateur | Esthétique | S'adapter harmonieusement au Robot |
| **FC5** | Pouvoir se ranger dans sa boîte d'origine (pare-chocs monté) | Profondeur, Longueur | Ne doit pas dépasser de 35 mm maxi devant le robot |
| **FC6** | Respecter le règlement du concours de robotique | Largeur | Largeur maximale autorisée 160 mm |
| **FC7** | Être fabriqué assez rapidement et sans consommer trop de matière | Énergie/Temps | - Impression 2h maxi<br>- Utiliser moins de 11m de fil d'impression |

---

## 2. Introduction au SysML

### Qu'est-ce que le SysML ?

**SysML** (System Modeling Language) est un outil graphique composé de diagrammes qui permettent d'aborder plus facilement les systèmes pluri-techniques. Il permet de représenter les objets techniques sous forme de schémas appelés **diagrammes**.

### Les diagrammes SysML permettent de représenter :

- ✓ Les **exigences** du système
- ✓ Les **composants** du système
- ✓ Les **flux** de toute nature (matière, énergie et information)
- ✓ Le **fonctionnement** du système

### Il y a 9 diagrammes SysML (tous ne sont pas au programme)

```
                        Diagrammes SysML
                               │
              ┌────────────────┼────────────────┐
              │                │                │
      Comportemental     Exigences        Structurel
              │                │                │
    ┌─────────┴─────────┐      │      ┌─────────┴──────────┐
    │                   │      │      │                    │
┌───┴────┐    ┌────────┴──┐   │   ┌──┴──────┐   ┌────────┴────┐
│Activité│    │États      │   │   │Définition│   │Blocs        │
│        │    │           │   │   │de blocs  │   │internes     │
└────────┘    └───────────┘   │   └──────────┘   └─────────────┘
                               │
    ┌──────────┐    ┌─────────┴────┐         ┌──────────┐
    │Séquence  │    │Cas           │         │Packages  │
    │          │    │d'utilisation │         │          │
    └──────────┘    └──────────────┘         └──────────┘
                          
                    ┌──────────────┐
                    │Paramétrique  │
                    └──────────────┘
```

---

## 3. Travaux à Faire - Corrections

### a. Diagramme d'Exigences du Pare-chocs

**Objectif** : C'est le cahier des charges fonctionnel du système (le système doit...). Ce sont les exigences du CDCF.

#### Correction du Diagramme d'Exigences

```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│    Pare-chocs robot pousseur                                │
│                                                              │
│    Permettre au robot de pousser les jantes                 │
│    sans sortir du circuit                                   │
│                                                              │
└────────────────────────┬─────────────────────────────────────┘
                         │
         ┌───────────────┼───────────────┐
         │               │               │
         │               │               │
    ┌────▼────┐    ┌─────▼─────┐   ┌────▼────┐
    │ Plaire à│    │ S'adapter │   │Le pare- │
    │ l'utili-│    │harmoni-   │   │chocs    │
    │ sateur  │    │eusement   │   │doit être│
    └────┬────┘    └─────┬─────┘   │conçu et │
         │               │          │réalisé  │
         │               │          │par des  │
    ┌────▼────┐    ┌─────▼─────┐   │élèves   │
    │Réalisable    │Géométrie  │   │de 3e    │
    │facilement    │compatible │   └────┬────┘
    │/rapidité │   │avec le    │        │
    └────┬────┘    │châssis    │        │
         │         └─────┬─────┘        │
         │               │              │
    ┌────▼────┐    ┌─────▼─────┐   ┌───▼────┐
    │Sans     │    │Respect du │   │Plastique│
    │modifi-  │    │règlement/ │   │         │
    │cation du│    │dimension  │   │Imprimante│
    │châssis  │    │national   │   │3D/Charly│
    └─────────┘    └─────┬─────┘   │robot/   │
                         │          │Solidworks│
                   ┌─────▼─────┐   └─────────┘
                   │Ne doit pas│
                   │toucher le │
                   │sol        │
                   └─────┬─────┘
                         │
                   ┌─────▼─────┐
                   │Doit pas   │
                   │dépasser   │
                   │dans la    │
                   │boîte      │
                   │d'origine  │
                   └─────┬─────┘
                         │
                   ┌─────▼─────┐
                   │Largeur    │
                   │maximale   │
                   │autorisée  │
                   │160 mm     │
                   └───────────┘
                         
    ┌───────────┐
    │Fabrication│
    │rapide     │
    └─────┬─────┘
          │
    ┌─────▼─────┐
    │Utiliser   │
    │moins de   │
    │11m de fil │
    │           │
    │Impression │
    │2h maxi    │
    └───────────┘
```

**Légende** :
- **▭** (rectangle plein) correspond à des **Fonctions Contraintes** (FC)
- **▭** (rectangle pointillé) correspond à des **niveaux d'exigences**

---

### b. Diagramme d'Utilisation

**Objectif** : Exprimer les services offerts par l'objet aux acteurs (Décris ce que fait l'objet, et non l'utilisateur, mais sans dire comment il le fait).

#### Correction du Diagramme d'Utilisation

```
┌──────────────────────────────────────────────────────────────────┐
│                    Robot + pare-chocs                            │
│                                                                  │
│  ┌──────────┐        ┌────────────────────────┐    ┌──────────┐ │
│  │          │        │ Sortir les jantes      │    │ Pare-    │ │
│  │Utilisateur◄───────┤ du circuit             ├────►chocs     │ │
│  │          │        └────────────────────────┘    │          │ │
│  │          │                                      │          │ │
│  │          │        ┌────────────────────────┐    │          │ │
│  │          ◄───────┤ Être programmé         ├────►Ordinateur│ │
│  │          │        └────────────────────────┘    │(carte de │ │
│  │          │                                      │ contrôle)│ │
│  │          │        ┌────────────────────────┐    │          │ │
│  │          ◄───────┤ Rester dans le circuit ├────►Capteur   │ │
│  │          │        └────────────────────────┘    │détecteur│ │
│  │          │                                      │          │ │
│  │          │        ┌────────────────────────┐    │          │ │
│  │          ◄───────┤ Se déplacer dans le    ├────►Roue      │ │
│  │          │        │ circuit                │    │          │ │
│  │          │        └────────────────────────┘    │          │ │
│  │          │                                      │          │ │
│  │          │        ┌────────────────────────┐    │Batterie  │ │
│  │          ◄───────┤ S'alimenter en énergie ├────►          │ │
│  └──────────┘        └────────────────────────┘    └──────────┘ │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

**Cas d'utilisation identifiés :**
1. **Sortir les jantes du circuit** (acteurs: Utilisateur, Pare-chocs)
2. **Être programmé** (acteurs: Utilisateur, Ordinateur/Carte de contrôle)
3. **Rester dans le circuit** (acteurs: Utilisateur, Capteur détecteur)
4. **Se déplacer dans le circuit** (acteurs: Utilisateur, Roues)
5. **S'alimenter en énergie** (acteurs: Utilisateur, Batterie)

---

### c. Diagramme d'Activité du Robot Pousseur

**Objectif** : Présenter le comportement de l'objet (le choix des actions en fonction de décisions).

**Contexte** : Notre robot pousseur doit suivre les jantes du circuit, sans jamais sortir de celui-ci. Il faudra donc détecter la ligne noire du circuit pour lui dire de s'arrêter et/ou de manœuvrer.

Pour démarrer, il faut appuyer sur l'interrupteur et le robot doit faire une petite séquence d'initialisation pendant 5s (musique, lumières).

#### Correction du Diagramme d'Activité

```
                          ┌─────────────────┐
                          │  ● (Début)      │
                          │  Appuyer sur    │
                          │  l'interrupteur │
                          └────────┬────────┘
                                   │
                          ┌────────▼────────┐
                         ╱                   ╲
                        ╱  Interrupteur      ╲
                       ◇   actionné ?         ◇
                        ╲                     ╱
                         ╲────────┬──────────╱
                                  │
                             Oui  │  Non
                  ┌───────────────┴───────────────┐
                  │                               │
                  ▼                               │
       ┌──────────────────────┐                   │
       │ Séquence             │                   │
       │ d'initialisation     │                   │
       │ (musique + lumière)  │                   │
       │ pendant 5s           │                   │
       └──────────┬───────────┘                   │
                  │                               │
       ┌──────────▼───────────┐                   │
       │ Détecter ligne Noire │                   │
       └──────────┬───────────┘                   │
                  │                               │
          ┌───────▼──────────┐                    │
         ╱                    ╲                   │
        ╱  Détection ligne     ╲                  │
       ◇   Noire ?              ◇─────────────────┘
        ╲                      ╱
         ╲────────┬───────────╱
                  │
   ┌──────────────┼──────────────┐
   │              │              │
   │ Gauche       │ Droite       │ Non détecté
   │              │              │
   ▼              ▼              ▼
┌──────────┐  ┌──────────┐  ┌──────────┐
│Détection │  │Détection │  │Détection │
│ligne     │  │ligne     │  │ligne     │
│Noire à   │  │Noire à   │  │Noire     │
│gauche    │  │droite    │  │devant    │
└────┬─────┘  └────┬─────┘  └────┬─────┘
     │             │             │
     ▼             ▼             ▼
┌──────────┐  ┌──────────┐  ┌──────────┐
│Reculer   │  │Reculer   │  │Reculer et│
│puis      │  │puis      │  │repartir à│
│tourner à │  │tourner à │  │gauche ou │
│gauche    │  │droite    │  │droite    │
│(2s)      │  │(2s)      │  │          │
└────┬─────┘  └────┬─────┘  └────┬─────┘
     │             │             │
     └─────────────┼─────────────┘
                   │
        ┌──────────▼──────────┐
        │ Continuer et pousser│
        │ les jantes          │
        └──────────┬──────────┘
                   │
                   │ (Retour à "Détecter ligne Noire")
                   └─────────────────────►
```

**Description du processus :**
1. L'utilisateur appuie sur l'interrupteur
2. Le robot vérifie si l'interrupteur est actionné
3. Si oui, il lance la séquence d'initialisation (5s avec musique et lumières)
4. Le robot commence à détecter la ligne noire
5. Selon la détection :
   - **Ligne à gauche** : Reculer et tourner à gauche (2s)
   - **Ligne à droite** : Reculer et tourner à droite (2s)
   - **Ligne devant** : Reculer et repartir à gauche ou droite
   - **Pas de ligne** : Continuer et pousser les jantes
6. Le cycle se répète en continu

---

### d. Diagramme des Blocs Internes

**Objectif** : Définir comment l'information, l'énergie et la matière circulent à travers l'objet.

#### Consignes
Tracez des flèches :
- **En vert et en pointillé** (─ ─ ─>) pour l'**information**
- **En rouge et en trait plein** (─────>) pour l'**énergie**
- Indiquez aussi la forme de l'énergie (EE, EM, lumière, son...)

#### Correction du Diagramme des Blocs Internes

```
┌─────────────────────────────────────────────────────────────────┐
│                   Diagramme des blocs internes                  │
│                   du robot pousseur avec pare-chocs             │
└─────────────────────────────────────────────────────────────────┘

                    ┌──────────────┐
                    │ Utilisateur  │
                    └──────┬───────┘
                           │
                           │ Information
                           │ (commandes)
                           │
    ┌──────────────────────▼────────────────────────┐
    │              Circuit principal                 │
    │                                               │
    │  ┌──────────────┐         Information        │
    │  │   Buzzer     │◄────────────────────────┐  │
    │  │              │                         │  │
    │  └──────────────┘                         │  │
    │         ▲                                 │  │
    │         │ Son                             │  │
    │         │                                 │  │
    │  ┌──────────────┐                         │  │
    │  │ Détecteur    │                         │  │
    │  │ de ligne     │                         │  │
    │  └──────┬───────┘                         │  │
    │         │                                 │  │
    │         │ Lumière (analogique)            │  │
    │         │                                 │  │
    │  ┌──────▼──────────────────────┐          │  │
    │  │  Carte de commande          ├──────────┘  │
    │  │  (Mbot)                     │             │
    │  └──────┬──────────────────────┘             │
    │         │                                    │
    │         │ Information                        │
    │         │                                    │
    │  ┌──────▼──────────┐                        │
    │  │ Circuit de      │                        │
    │  │ puissance       │                        │
    │  └──────┬──────────┘                        │
    │         │                                    │
    │         │ EM (Énergie Mécanique)             │
    │         │                                    │
    │  ┌──────▼──────────┐                        │
    │  │ Moteurs +       │                        │
    │  │ Roues           │                        │
    │  └──────┬──────────┘                        │
    │         │                                    │
    │         │ Mouvement/EM                       │
    │         │                                    │
    └─────────┼────────────────────────────────────┘
              │
              │ Mouvement/EM
              │
    ┌─────────▼─────────────────────────────────┐
    │                                           │
    │         ┌──────────────┐                  │
    │         │ Capteur      │                  │
    │         │ Ultrason     │                  │
    │         └──────┬───────┘                  │
    │                │                          │
    │                │ Analogique               │
    │                │                          │
    │         ┌──────▼───────┐                  │
    │         │ Carte de     │                  │
    │         │ commande     │                  │
    │         └──────▲───────┘                  │
    │                │                          │
    │                │ EE (Énergie Électrique)  │
    │                │                          │
    │         ┌──────┴───────┐                  │
    │         │ Énergie      │                  │
    │         │(alimentation)│                  │
    │         │ Batterie     │                  │
    │         └──────────────┘                  │
    │                                           │
    └───────────────────────────────────────────┘
              │
              │ EM
              │
    ┌─────────▼─────────────────────────────────┐
    │            Jantes                         │
    │                                           │
    │         ┌──────────────┐                  │
    │         │ Pare-chocs   │                  │
    │         └──────────────┘                  │
    │                                           │
    │         ┌──────────────┐                  │
    │         │ Châssis      │                  │
    │         └──────────────┘                  │
    │                                           │
    └───────────────────────────────────────────┘
```

**Composants identifiés et leurs flux :**

| Composant | Type de flux (Entrée) | Type de flux (Sortie) |
|-----------|----------------------|----------------------|
| **Utilisateur** | - | Information (commandes) |
| **Carte de commande** | Information (capteurs) | Information (contrôle) |
| **Circuit de puissance** | Information + EE | EM (vers moteurs) |
| **Moteurs + Roues** | EM | Mouvement/Déplacement |
| **Buzzer** | Information (signal) | Son |
| **Détecteur de ligne** | Lumière réfléchie | Signal analogique |
| **Capteur Ultrason** | - | Signal analogique |
| **Alimentation (Batterie)** | - | EE (Énergie Électrique) |
| **Pare-chocs** | Force/Matière | Transmission de force |
| **Châssis** | Support mécanique | Support structure |
| **Jantes** | Force (poussée) | Déplacement |

**Légende des types d'énergie :**
- **EE** : Énergie Électrique
- **EM** : Énergie Mécanique
- **Information** : Données numériques, signaux analogiques
- **Matière** : Objets physiques (jantes)

---

## 4. La « Pieuvre » : Le Graphe des Interactions

**Objectif** : Visualiser les interactions entre le pare-chocs et son environnement.

#### Éléments du graphe

```
          ┌──────────────┐
          │ ROBOT MBOT   │
          └──────┬───────┘
            FC6  │
          ┌──────▼───────┐
          │  Pare-Choc   │◄──────FP1──────┐
          └──┬───┬───┬───┘                │
         FC5 │   │   │ FC4           ┌────▼────┐
             │   │   │               │ Jantes  │
    ┌────────▼┐  │  ┌▼────────┐     └─────────┘
    │ Boîte   │  │  │Utilisateur│
    │ d'origine│ │  └─────────┘
    └─────────┘  │       │
              FC3│      FC2
          ┌──────▼───┐  │
          │ Collège  │  │
          └──────────┘  │
              │      FC7│
          ┌───▼─────────▼┐
          │ Fabrication  │
          └───┬──────────┘
              │
          ┌───▼──────┐
          │   SOL    │
          └──────────┘
```

**Consignes** : Établir le lien entre la « pieuvre » et le CDCF en coloriant chaque ligne du tableau d'une couleur différente et colorie de la même couleur l'élément de la pieuvre correspondant.

**Correspondance Pieuvre ↔ CDCF :**

| Fonction | Élément 1 | Élément 2 | Description |
|----------|-----------|-----------|-------------|
| **FP1** | Pare-chocs | Jantes | Permettre au robot de pousser les jantes |
| **FC1** | Pare-chocs | Collège | Être réalisable au collège |
| **FC2** | Pare-chocs | Sol | Ne doit pas toucher le sol |
| **FC3** | Pare-chocs | Robot Mbot | S'adapter au châssis du robot Mbot |
| **FC4** | Pare-chocs | Utilisateur | Adaptation pour plaire à l'utilisateur |
| **FC5** | Pare-chocs | Boîte d'origine | Pouvoir se ranger dans sa boîte d'origine |
| **FC6** | Pare-chocs | Robot Mbot | Respecter le règlement du concours |
| **FC7** | Pare-chocs | Fabrication | Être fabriqué rapidement et économiquement |

---

## 5. Résumé des Concepts Clés

### Les 9 Diagrammes SysML

#### Diagrammes Comportementaux
1. **Diagramme d'activité** - Comportement, algorithme, processus
2. **Diagramme d'états** - États du système et transitions
3. **Diagramme de séquence** - Chronologie des actions et interactions
4. **Diagramme de cas d'utilisation** - Services rendus aux acteurs

#### Diagramme d'Exigences
5. **Diagramme d'exigences** - Cahier des charges, spécifications

#### Diagrammes Structurels
6. **Diagramme de définition de blocs** - Structure du système
7. **Diagramme de blocs internes** - Flux (matière, énergie, information)
8. **Diagramme de packages** - Organisation modulaire
9. **Diagramme paramétrique** - Paramètres et contraintes mathématiques

### Catégories principales
- **Fonctionnel** : Que doit faire le système ?
- **Comportementaux** : Comment le système se comporte-t-il ?
- **Structurels** : Comment le système est-il structuré ?

---

## 6. Vocabulaire Important

| Terme | Définition |
|-------|------------|
| **CDCF** | Cahier Des Charges Fonctionnel |
| **FP** | Fonction Principale - Ce que fait le système |
| **FC** | Fonction Contrainte - Les limites du système |
| **SysML** | System Modeling Language - Langage de modélisation |
| **EE** | Énergie Électrique |
| **EM** | Énergie Mécanique |
| **Information** | Données, signaux de contrôle |
| **Matière** | Flux d'objets physiques |
| **Acteur** | Élément qui interagit avec le système |

---

## 7. Conseils pour l'Élève

✓ **Bien comprendre la différence entre les types de diagrammes** - Chaque diagramme a un objectif précis

✓ **Identifier clairement les flux** - Distinguer information, énergie et matière

✓ **Respecter les symboles normalisés du SysML** - Utiliser les bonnes formes (losanges pour décisions, rectangles pour actions, etc.)

✓ **Lire attentivement le CDCF avant de commencer** - C'est la base de tout le projet

✓ **Vérifier que chaque exigence est respectée dans la conception** - Traçabilité des exigences

✓ **Penser aux interactions avec l'environnement** - Le système ne fonctionne pas seul

✓ **Utiliser les bons outils** - SolidWorks, Charlyrobot, imprimante 3D

---

## 8. Méthodologie de Travail

### Étapes de conception d'un système

1. **Analyser le besoin** (Diagramme de cas d'utilisation)
2. **Définir les exigences** (Diagramme d'exigences, CDCF)
3. **Identifier les interactions** (Pieuvre)
4. **Structurer le système** (Diagramme de blocs)
5. **Définir le comportement** (Diagramme d'activité)
6. **Modéliser en 3D** (SolidWorks)
7. **Fabriquer** (Impression 3D)
8. **Tester et valider** (Vérifier les exigences)

---

## 9. Critères d'Évaluation du Projet

| Critère | Points clés à vérifier |
|---------|------------------------|
| **Respect du CDCF** | Toutes les FC sont respectées |
| **Fonctionnalité** | Le robot pousse bien les jantes |
| **Fabrication** | Temps < 2h, fil < 11m |
| **Esthétique** | Design harmonieux |
| **Documentation** | Diagrammes SysML complets |
| **Innovation** | Solutions créatives |

---

## Annexes

### Ressources utiles
- Documentation SysML
- Tutoriels SolidWorks
- Guide d'utilisation de l'imprimante 3D
- Règlement du concours de robotique

### Outils logiciels
- **SolidWorks** : Modélisation 3D
- **Charlygraal** : Programmation Charlyrobot
- **Logiciel de découpe** : Préparation impression 3D
- **Mblock** : Programmation du robot Mbot

---

*Fin du cours de synthèse - Robot Pousseur avec Pare-chocs*

**Date** : 3ème année Collège  
**Matière** : Technologie  
**Thème** : Conception numérique et impression 3D

---

## Pour aller plus loin

- Recherche sur les systèmes de détection de lignes
- Étude des différents types de capteurs
- Optimisation de la forme du pare-chocs
- Programmation avancée du robot
- Analyse des performances en situation réelle
