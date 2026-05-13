# LAB2
🧪 LAB 2 : Rooting Android

Cours : Sécurité des applications mobiles

1. 📘 Vue d’ensemble

Ce lab consiste à comprendre et expérimenter le rooting Android dans un environnement contrôlé (AVD), ainsi que ses impacts sur la sécurité.

2. ⚡ Avant de commencer (2 min)
Utiliser un environnement de test (AVD recommandé)
Ne jamais rooter un téléphone personnel
Vérifier que ADB fonctionne
3. 🔓 Étape 1 : Rooter l’AVD
Commandes :
adb root
adb remount
🔗 Capture 1 — ADB root

<img width="538" height="289" alt="1" src="https://github.com/user-attachments/assets/e2738a41-9d38-4441-8528-7e710c02c643" />


📌 Résultat attendu :

adbd is already running as root
4. 📄 Étape 2 : Fiche périmètre (5 lignes)
Environnement : AVD Android
Objectif : tester sécurité post-root
Outils : ADB
Cible : OS Android
Risque : accès total système
5. 🔁 Étape 3 : Démarrer un AVD propre
🔗 Capture 2 — AVD Manager

<img width="336" height="370" alt="2" src="https://github.com/user-attachments/assets/ea07763f-89b4-4263-8ddc-ef904bdac2ea" />


📌 Résultat :

Émulateur démarré
6. 📲 Étape 4 : Installer et lancer l’app de test
Commande :
adb install app.apk
🔗 Capture 3 — Installation APK

<img width="593" height="315" alt="3" src="https://github.com/user-attachments/assets/c00cb6b7-0348-4142-8969-855ae5c07fcf" />


7. 🧠 Étape 5 : Définir 3 scénarios simples
Application détecte le root → bloque accès
Application fonctionne → mais vulnérable
Application exploite root → accès données
8. 📖 Étape 6 : Lire Android Security (6 lignes)

Android repose sur :

sandbox des applications
permissions
isolation processus
vérification du boot
chiffrement
contrôle utilisateur
9. 🔐 Étape 7 : Verified Boot

Android vérifie l’intégrité du système au démarrage.
Si modification → alerte sécurité.

10. 🔐 Étape 8 : AVB (Android Verified Boot)

AVB garantit que :

système non modifié
partitions signées
chaîne de confiance respectée
11. 🧾 Étape 9 : Définir le rooting (4 phrases)

Le rooting consiste à obtenir les droits administrateur sur Android.
Il permet de modifier le système.
Il contourne les protections natives.
Il expose le système à des risques élevés.

12. 🎯 Étape 10 : Intérêt du labo
Comprendre les failles
Tester sécurité
Simuler attaquant
13. ⚠️ Étape 11 : Matrice de risques (8)
Accès root malveillant
Vol de données
Malware système
Désactivation protections
Altération OS
Escalade privilèges
Fuite données
Backdoor
14. 🛡️ Étape 12 : Mesures défensives (8)
Détection root
Chiffrement données
Vérification intégrité
Code sécurisé
Obfuscation
Permissions minimales
Mise à jour OS
Monitoring
15. 📏 Étape 13 : OWASP MASVS
MASVS-RESILIENCE
MASVS-PLATFORM
16. 🔍 Étape 14 : OWASP MASTG
Test détection root
Test bypass sécurité
17. 💻 Étape 15 : Commandes de rooting
adb root
adb remount
adb shell
su
18. 📋 Étape 16 : Traçabilité (environnement)
OS : Windows i5
VM : Mobexler
AVD : Android Emulator
Outils : ADB
19. 🔄 Étape 17 : Reset AVD

👉 Supprimer et recréer AVD

20. 🔄 Étape 18 : Reset device

👉 Redémarrer ou factory reset

21. 📄 Étape 19 : Livrables
Rapport 1–2 pages
Screenshots
Analyse
22. ✅ Étape 20 : Checklist finale
AVD rooté
App testée
Risques identifiés
Défenses proposées
📚 Ressources & Glossaire
ADB : communication Android
AVD : émulateur
Bootloader : démarrage
Fastboot : flash
Root : admin
Sandbox : isolation
AVB : sécurité boot
📊 Schémas

Architecture :

Matériel → Bootloader → Kernel → Android → Apps

Root impact :

Normal : sécurisé
Rooté : modifiable
