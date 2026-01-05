# TP 30 — Pipeline CI/CD avec Jenkins, GitHub, Docker et ngrok

## 🚀 Aperçu

Dans ce TP, nous mettons en place un **pipeline CI/CD complet** pour une application Spring Boot :

- 📥 Récupération automatique du code depuis **GitHub**
- 🔨 Build Maven + exécution des tests
- 🐳 Construction d’une **image Docker**
- ▶️ Lancement automatique du conteneur Docker
- 🔔 Déclenchement automatique du pipeline via **GitHub Webhook** exposé par **ngrok**

Ce TP illustre la chaîne DevOps moderne : **développer ➜ tester ➜ construire ➜ déployer automatiquement**.

---

## 🎯 Objectifs pédagogiques

À la fin du TP, vous serez capable de :

✔️ Expliquer la différence entre **CI** (Intégration Continue) et **CD** (Livraison/Déploiement Continu)  
✔️ Installer et configurer **Jenkins**  
✔️ Configurer **Maven** dans Jenkins  
✔️ Créer un pipeline Jenkins pour un projet Spring Boot  
✔️ Construire une image Docker automatiquement  
✔️ Exposer Jenkins via **ngrok**  
✔️ Configurer un **webhook GitHub** déclenchant le pipeline automatiquement

---

## 🧰 Pré-requis

- 🪟 Windows 10 / 11  
- ☕ Java JDK 17 ou 21  
- 🐙 Git installé  
- 🐳 Docker Desktop installé et démarré  
- 🧑‍💻 Compte GitHub  
- 🌍 Accès Internet  

> ⚠️ **Important :**  
> Jenkins doit pouvoir exécuter Docker.  
> Si Jenkins tourne comme **service Windows**, vérifier que le compte Jenkins a accès au daemon Docker.

---

## 📌 Rappel : CI, CD et Pipeline

### 🔁 Intégration Continue (CI)

À chaque push :

- compilation
- exécution des tests
- retour rapide des erreurs

🎯 Objectif : **détecter les problèmes tôt**.

---

### 🚚 Livraison / Déploiement Continu (CD)

Automatise :

- la création d’artefacts (jar, images Docker…)
- leur déploiement contrôlé

Dans ce TP :

👉 la CD correspond à la **création et l’exécution automatique d’une image Docker**.

---

### 🧩 Pipeline CI/CD typique

1️⃣ Développeur fait un **push** sur GitHub  
2️⃣ Jenkins détecte le changement (webhook)  
3️⃣ Jenkins build + tests  
4️⃣ Création de l’image Docker  
5️⃣ Lancement du conteneur

---



