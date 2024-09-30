Voici un fichier README adapté pour votre TP avec des espaces pour les captures d’écran.

---

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

_**Capture d'écran :**_
```
[Capture d'écran de la fenêtre "New Project"]
```

5. Cliquez sur **Finish** pour créer le projet.

### Intégration du Driver MySQL
1. Cliquez avec le bouton droit sur le projet et sélectionnez **Properties**.
2. Dans l'onglet **Libraries**, cliquez sur **Add Library** et ajoutez le driver MySQL.

_**Capture d'écran :**_
```
[Capture d'écran de l'ajout du driver MySQL]
```

## Partie 2 : Création de la table Site

1. Ouvrez votre console MySQL et connectez-vous à la base de données `db`.
2. Créez la table `Site` avec la commande suivante :

```sql
CREATE TABLE Site (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  location VARCHAR(100)
);
```

_**Capture d'écran :**_
```
[Capture d'écran de la création de la table Site dans MySQL]
```

## Partie 3 : Insertion des données

1. Dans NetBeans, créez une classe `Site` dans le package `beans` pour représenter un site avec ses attributs.
2. Créez la méthode `save(Site site)` dans une classe `Test` pour insérer des données dans la table `Site`.

_**Capture d'écran :**_
```
[Capture d'écran de la classe Site et méthode save()]
```

### Exemple de code pour la méthode `save` :

```java
public void save(Site site) {
    Connection conn = getConnection();
    String query = "INSERT INTO Site (name, location) VALUES (?, ?)";
    try (PreparedStatement stmt = conn.prepareStatement(query)) {
        stmt.setString(1, site.getName());
        stmt.setString(2, site.getLocation());
        stmt.executeUpdate();
    } catch (SQLException e) {
        e.printStackTrace();
    }
}
```

3. Testez la méthode `save()` dans la méthode `main` :

_**Capture d'écran :**_
```
[Capture d'écran des résultats de l'insertion des données]
```

## Partie 4 : Récupération des données

1. Ajoutez une méthode `load()` dans la classe `Test` pour récupérer les sites enregistrés dans la base de données.

_**Capture d'écran :**_
```
[Capture d'écran de la méthode load()]
```

### Exemple de code pour la méthode `load` :

```java
public List<Site> load() {
    List<Site> sites = new ArrayList<>();
    Connection conn = getConnection();
    String query = "SELECT * FROM Site";
    try (Statement stmt = conn.createStatement()) {
        ResultSet rs = stmt.executeQuery(query);
        while (rs.next()) {
            Site site = new Site(rs.getInt("id"), rs.getString("name"), rs.getString("location"));
            sites.add(site);
        }
    } catch (SQLException e) {
        e.printStackTrace();
    }
    return sites;
}
```

2. Testez la méthode `load()` dans la méthode `main` :

_**Capture d'écran :**_
```
[Capture d'écran des résultats de la récupération des données]
```

---

### Conclusion

Ce TP vous a permis de comprendre comment créer un projet Java avec NetBeans, connecter ce projet à une base de données MySQL, insérer des données, et les récupérer via des méthodes Java.

---

Ajoutez vos captures d’écran au fur et à mesure pour documenter le processus dans ce fichier README.

