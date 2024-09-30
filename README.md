
# TP1 : Insertion et récupération des données

**Réaliser par :**  
GRIMA FATIMA ZAHRA

**Encadré par :**  
Pr. LACHGAR

**Année universitaire :**  
2024/2025

## Table des matières
1. [Introduction](#introduction)
2. [Partie 1 : Projet NetBeans `demojdbc`](#partie-1--projet-netbeans-demojdbc)
3. [Partie 2 : Création de la table Site](#partie-2--création-de-la-table-site)
4. [Partie 3 : Insertion des données](#partie-3--insertion-des-données)
5. [Partie 4 : Récupération des données](#partie-4--récupération-des-données)

---

## Introduction

Dans ce TP, nous allons créer un projet Java avec NetBeans, insérer et récupérer des données dans une base de données MySQL. Nous allons également créer des méthodes Java pour interagir avec la base de données.

## Partie 1 : Projet NetBeans `demojdbc`

### Création du projet
1. Ouvrez NetBeans.
2. Cliquez sur **Menu** > **File** > **New Project**.
3. Sélectionnez **Java** puis **Java Application** et cliquez sur **Next**.
4. Entrez le nom du projet : `demojdbc`.


![image](https://github.com/user-attachments/assets/4384263d-b4ed-4e42-9b33-b18cfae0fe75)

5. Cliquez sur **Finish** pour créer le projet.

### Intégration du Driver MySQL
1. Cliquez avec le bouton droit sur le projet et sélectionnez **Properties**.
2. Dans l'onglet **Libraries**, cliquez sur **Add Library** et ajoutez le driver MySQL.


![image](https://github.com/user-attachments/assets/b898ca26-21cb-44eb-a814-7a31f9c63fb5)



## Partie 2 : Création de la table Site

1. Ouvrez votre console MySQL et connectez-vous à la base de données `db`.
2. Créez la table `Site` avec la commande suivante :

![image](https://github.com/user-attachments/assets/0bd16d4f-710e-46ee-aa00-04d5759e2a7f)


![image](https://github.com/user-attachments/assets/deef2d88-cccd-48a5-bcd9-49120c882263)


## Partie 3 : Insertion des données

1. Dans NetBeans, créez une classe `Site` dans le package `beans` pour représenter un site avec ses attributs.
2. Créez la méthode `save(Site site)` dans une classe `Test` pour insérer des données dans la table `Site`.

![image](https://github.com/user-attachments/assets/4c186b00-67fd-4a76-bfed-f9e4c0d77538)

![image](https://github.com/user-attachments/assets/a29edc41-40e8-4913-a6be-303685b697fd)




3. Testez la méthode `save()` dans la méthode `main` :

![image](https://github.com/user-attachments/assets/eed105e4-0e28-45d9-9003-fb5d02981cd7)

![image](https://github.com/user-attachments/assets/8ff55b90-1a13-4a97-b9a8-3e49dd22eeb8)



## Partie 4 : Récupération des données

1. Ajoutez une méthode `load()` dans la classe `Test` pour récupérer les sites enregistrés dans la base de données.

![image](https://github.com/user-attachments/assets/b86b8b6e-5218-4444-8349-0af80289c664)



2. Testez la méthode `load()` dans la méthode `main` :

![image](https://github.com/user-attachments/assets/34c83003-a48e-4a46-bd1e-2be09b59dc61)

![image](https://github.com/user-attachments/assets/1f25ef7f-a886-4c2d-ad67-29aac53ca768)



### Conclusion

Ce TP m'a permis de comprendre comment créer un projet Java avec NetBeans, connecter ce projet à une base de données MySQL, insérer des données, et les récupérer via des méthodes Java.

---

