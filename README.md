# 🛒 SuperMarché Online

![Status](https://img.shields.io/badge/status-En%20développement-orange)
![Java EE](https://img.shields.io/badge/Java%20EE-ED8B00?style=flat&logo=java&logoColor=white)
![JSP](https://img.shields.io/badge/JSP-FF0000?style=flat&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=flat&logo=mysql&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![License](https://img.shields.io/badge/license-Academic-blue)

---

## 🌐 Présentation

**SuperMarché Online** est une application web complète
de gestion d'un supermarché en ligne avec plusieurs
niveaux d'administration.

Elle offre deux espaces distincts :

- 🛍️ Parcourir, commander et suivre des produits
- 📦 Gérer produits, stocks, commandes et clients
- 👥 Système multi-rôles pour répartir les responsabilités
- 🔐 Plateforme sécurisée avec gestion des sessions
- 📊 Tableau de bord complet pour les administrateurs
- 🔔 Alertes automatiques sur les stocks faibles

> 💡 Projet réalisé dans le cadre du cours de
> **Développement Web Full Stack — Java EE**
> Présenté par l'équipe · 2024

---

## 👥 Utilisateurs & Rôles

🔑 **Super Administrateur**
→ Supervise tout le système
→ Crée, modifie et supprime les administrateurs
→ Accès total à toutes les fonctionnalités

📦 **Administrateur Produits & Catégories**
→ Gère le catalogue complet du supermarché
→ Ajoute, modifie et supprime produits et catégories
→ Gère les comptes clients

📊 **Administrateur Stock & Commandes**
→ Gère les stocks et quantités disponibles
→ Confirme et met à jour le statut des commandes
→ Gère les produits en rupture de stock

🛒 **Client**
→ Crée un compte et se connecte
→ Parcourt, recherche et commande des produits
→ Consulte l'historique de ses commandes

---

## 🚀 Fonctionnalités

### 🔐 Authentification
- Inscription avec nom, prénom, email, téléphone
- Connexion sécurisée avec gestion de session
- Modification du profil et changement de photo
- Réinitialisation du mot de passe
- Redirection automatique selon le rôle

### 🗂️ Gestion des Catégories
- Ajouter / Modifier / Supprimer une catégorie
- Afficher toutes les catégories disponibles
- Catégories : 🥛 Produits Laitiers · 🥦 Fruits & Légumes
  · 🥤 Boissons · 🍞 Boulangerie · 🍫 Snacks
  · 🧹 Ménager · 🍳 Accessoires Cuisine · 🧊 Surgelés

### 📦 Gestion des Produits
- Ajouter un produit : nom, prix, image, stock, catégorie
- Modifier ou supprimer un produit du catalogue
- Afficher les produits par catégorie
- Afficher les produits en rupture de stock

### 📊 Gestion du Stock
- Afficher la quantité disponible par produit
- Alerte automatique si stock faible
- Mise à jour automatique après chaque commande
- Gestion des produits en rupture

### 🛒 Panier
- Ajouter / modifier quantité / supprimer un article
- Voir le prix total en temps réel
- Validation avant passage de commande

### 📋 Commandes
- Passer une commande depuis le panier
- Suivre le statut en temps réel :
  `⏳ En attente` → `✅ Confirmée` → `🔧 En préparation` → `🚚 En livraison` → `📦 Livrée`
- Annulation possible selon le statut

### 🖥️ Tableau de Bord Admin
- Nombre total de produits, commandes et clients
- Alertes produits en rupture de stock
- Commandes récentes avec statuts
- Statistiques globales du système

---

## 🛠️ Stack Technique

### 🎨 Frontend
![JSP](https://img.shields.io/badge/JSP-FF0000?style=for-the-badge&logo=java&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### 🔧 Backend
![Java](https://img.shields.io/badge/Java%20EE-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Servlets](https://img.shields.io/badge/Servlets-007396?style=for-the-badge&logo=java&logoColor=white)
![JSP](https://img.shields.io/badge/JSP-FF0000?style=for-the-badge&logo=java&logoColor=white)
![JDBC](https://img.shields.io/badge/JDBC-007396?style=for-the-badge&logo=java&logoColor=white)
![Tomcat](https://img.shields.io/badge/Tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=black)

### 🗄️ Base de données
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

### 🔨 Outils
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
![Eclipse](https://img.shields.io/badge/Eclipse-2C2255?style=for-the-badge&logo=eclipse&logoColor=white)

---

## ⚙️ Installation

### Prérequis
- Java JDK 11+
- Apache Tomcat 9+
- MySQL 8+
- Eclipse IDE (Java EE)

### Étapes
```bash
# 1. Cloner le projet
git clone https://github.com/votre-repo/SupermarcheOnline.git
cd SupermarcheOnline

# 2. Créer la base de données
mysql -u root -p
CREATE DATABASE supermarche_db;
USE supermarche_db;

# 3. Configurer la connexion DB
# Modifier src/main/java/util/DBConnection.java
private static final String URL =
    "jdbc:mysql://localhost:3306/supermarche_db";
private static final String USER = "root";
private static final String PASSWORD = "votre_mot_de_passe";

# 4. Importer dans Eclipse
File → Import → Existing Projects into Workspace

# 5. Configurer Tomcat
Clic droit projet → Run As → Run on Server
Sélectionner Apache Tomcat 9

# 6. Accéder à l'application
http://localhost:8080/SupermarcheOnline
```

---

## 👨‍💻 Équipe

👤 **Bendaoud Adam** — Développeur Full Stack
👤 **Faycal Lahri** — Développeur Full Stack
👤 **Mootya Salma** — Développeur Full Stack

👩‍🏫 **Encadré par :** Mme. Chaimae Zaoui

---

## 📄 Licence

Ce projet est réalisé dans un cadre académique — **2024**.
Tous droits réservés à l'équipe **Bendaoud · Lahri · Mootya**.

---

<p align="center">
  Réalisé avec ❤️ par 
  <strong>Bendaoud Adam · Faycal Lahri · Mootya Salma</strong> 
  — 2024
</p>
