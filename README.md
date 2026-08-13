# Atelier NumPy — Analyse de données IoT

##  Présentation du projet

Ce projet consiste à mettre en pratique la bibliothèque **NumPy** dans le cadre de l'analyse de données issues de capteurs IoT.

L'objectif de cet atelier est de manipuler, explorer et analyser des données de température provenant de plusieurs capteurs installés dans différents bâtiments.

À travers différentes manipulations, les données sont générées, transformées, filtrées et analysées afin de développer les bases nécessaires à la **préparation de données pour un futur système de Machine Learning** capable notamment de détecter des situations anormales.

---

##  Objectifs

Au cours de cet atelier, j'ai appris à utiliser NumPy pour :

* créer et manipuler des tableaux numériques ;
* comparer le comportement des listes Python avec celui des tableaux NumPy ;
* générer des données numériques et aléatoires ;
* explorer les caractéristiques d'un tableau ;
* accéder aux données avec l'indexation et le slicing ;
* filtrer des données à l'aide de conditions booléennes ;
* manipuler des matrices et leurs dimensions ;
* concaténer plusieurs tableaux ;
* effectuer des calculs statistiques ;
* standardiser et normaliser des données ;
* utiliser le broadcasting ;
* appliquer des corrections automatiquement sur des données ;
* préparer des données numériques pour une utilisation future en Machine Learning.

---

##  Travail réalisé

### 1. Comparaison entre Python et NumPy

J'ai commencé par comparer une **liste Python** avec un **tableau NumPy** contenant les mêmes températures.

Cette comparaison m'a permis de comprendre une différence importante dans le comportement des opérations mathématiques. Avec une liste Python, la multiplication par un nombre répète les éléments de la liste, tandis qu'avec un tableau NumPy, elle effectue une opération mathématique sur chaque valeur.

Cette première manipulation permet donc de comprendre l'intérêt des tableaux NumPy pour le calcul scientifique.

---

### 2. Création et génération de données

J'ai utilisé NumPy pour créer différents types de tableaux :

* tableaux initialisés avec des zéros ;
* tableaux initialisés avec des uns ;
* tableaux contenant une valeur constante ;
* matrice identité ;
* tableau représentant les 24 heures d'une journée ;
* valeurs régulièrement espacées entre deux températures ;
* données générées aléatoirement.

La génération aléatoire a également été rendue **reproductible** grâce à l'utilisation d'une graine aléatoire (`seed`).

---

### 3. Exploration des tableaux

J'ai ensuite analysé les caractéristiques des tableaux générés.

Les propriétés étudiées permettent notamment de connaître :

* le nombre de dimensions ;
* le nombre total de valeurs ;
* le type des données ;
* la forme du tableau.

Cela permet de mieux comprendre la structure des données avant de les manipuler.

---

### 4. Indexation et slicing

J'ai manipulé un tableau représentant les températures mesurées pendant les 24 heures d'une journée.

J'ai notamment réalisé des opérations permettant de :

* récupérer la première mesure ;
* récupérer la dernière mesure ;
* accéder à une mesure correspondant à une heure précise ;
* extraire une plage horaire ;
* récupérer les premières mesures ;
* sélectionner les mesures correspondant aux heures paires.

Cette partie m'a permis de mettre en pratique **l'indexation et le slicing NumPy**.

---

### 5. Détection des températures inhabituelles

J'ai utilisé le **filtrage booléen** pour analyser les températures et identifier les valeurs pouvant représenter des situations inhabituelles.

Différents critères ont été appliqués afin de :

* sélectionner les températures supérieures à 30 °C ;
* identifier les températures comprises entre 20 °C et 30 °C ;
* détecter les températures supérieures à 35 °C ;
* créer un tableau booléen indiquant les anomalies ;
* compter le nombre de températures considérées comme anormales.

Cette manipulation constitue une première approche de la **détection d'anomalies** dans des données de capteurs.

---

### 6. Manipulation des matrices

J'ai ensuite travaillé avec une matrice représentant les températures de plusieurs capteurs pendant une journée.

J'ai réalisé différentes opérations sur cette matrice :

* transformation d'une matrice en tableau unidimensionnel ;
* calcul de sa transposée ;
* extraction des données d'un capteur ;
* extraction des mesures d'une heure précise ;
* extraction d'une partie de la matrice selon les capteurs et les heures.

Cette partie m'a permis de mieux comprendre la manipulation des **tableaux multidimensionnels avec NumPy**.

---

### 7. Fusion des données de plusieurs bâtiments

Les données d'un deuxième bâtiment équipé de plusieurs capteurs ont été générées afin de simuler un environnement comportant plusieurs sources de données.

J'ai ensuite fusionné les données des différents capteurs grâce à différentes méthodes de concaténation NumPy.

L'objectif était d'obtenir une seule matrice regroupant les mesures provenant des différents bâtiments.

---

### 8. Analyse statistique

J'ai effectué plusieurs calculs statistiques sur les températures :

* minimum ;
* maximum ;
* somme ;
* moyenne ;
* médiane ;
* variance ;
* écart-type.

J'ai également appliqué deux transformations couramment utilisées dans la préparation des données :

**Standardisation**

Les températures ont été standardisées afin d'obtenir des données centrées autour de 0 avec un écart-type proche de 1.

**Normalisation Min-Max**

Les données ont également été normalisées afin de les ramener dans une plage commune.

Enfin, les températures ont été converties de **Celsius vers Fahrenheit**.

---

### 9. Utilisation du Broadcasting

J'ai mis en pratique le **broadcasting NumPy** sur des données représentant les températures mesurées pendant plusieurs jours.

Des valeurs de correction propres aux capteurs ont été stockées dans un tableau :

```python
correction = np.array([1, -0.5, 0.2])
```

Ces corrections ont ensuite été appliquées directement aux mesures :

```python
mesures_corrigees = temperatures_vsd + correction
```

Cette manipulation montre comment NumPy peut effectuer automatiquement des opérations entre des tableaux de dimensions compatibles sans avoir besoin de parcourir explicitement chaque valeur avec une boucle.

---

##  Technologies utilisées

| Technologie          | Utilisation                                          |
| -------------------- | ---------------------------------------------------- |
| **Python**           | Langage de programmation                             |
| **NumPy**            | Création et manipulation des tableaux numériques     |
| **Jupyter Notebook** | Environnement d'exécution et présentation du travail |
| **Git**              | Gestion des versions                                 |
| **GitHub**           | Hébergement du projet                                |

---

##  Structure du projet

```text
atelier_numpy_iot/
│
├── atelier_numpy_iot.ipynb
│
└── README.md
```

Le fichier `atelier_numpy_iot.ipynb` contient l'ensemble des manipulations, calculs et résultats réalisés pendant l'atelier.

---

##  Exécution

### Prérequis

* Python 3.x
* NumPy
* Jupyter Notebook ou Visual Studio Code

### Installation de NumPy

```bash
pip install numpy
```

### Lancement du notebook

Ouvrir le fichier :

```text
atelier_numpy_iot.ipynb
```

Puis exécuter les cellules du notebook dans l'ordre.

---

## Compétences développées

Ce projet m'a permis de renforcer mes connaissances en **Python et en calcul numérique avec NumPy**, notamment sur :

* les tableaux `ndarray` ;
* les tableaux multidimensionnels ;
* l'indexation ;
* le slicing ;
* les masques booléens ;
* les fonctions statistiques ;
* les nombres aléatoires ;
* la manipulation des dimensions ;
* la concaténation ;
* le broadcasting ;
* la standardisation ;
* la normalisation.

Ces notions constituent une base importante pour la **data science**, l'analyse de données et la préparation des données destinées au Machine Learning.

