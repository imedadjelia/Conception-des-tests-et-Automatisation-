# Conception-des-tests-et-Automatisation-
Conception des tests pour "IT-akademy" et Automatisation avec Selenium et Pytest
Dans le cadre du module "Introduction aux web services et API", nous avons réalisé un TP visant à valider les fonctionnalités d'une API pour un système de gestion de location de véhicules. 

Conception des tests 
[Conception des tests](https://docs.google.com/document/d/1o1g3CfSvPM0GjFFmtMKfW6YT3fQpt8lLYnLovWd1pS8/edit)

#Conception des Tests 
##Projet :  Tester le site web de l’it-akademy «https://inscription.it-akademy.fr/»
##Objectif :  It-akademy souhaite valider les fonctionnalités présentent sur sont site web «https://inscription.it-akademy.fr/ » avant une mise en production : 
*L’utilisateur pour s’inscrire à l'une des formations doit se connecter à l’écran de connexion « Plateforme admissions ». Si l’ utilisateur ne dispose pas de compte , il doit pouvoir créer son compte via l’écran « Nouveau compte ». Si l’ utilisateur a oublié son mot de passe , il peut demander une réinitialisation via l’écran « Mot de passe oublié ». une case à cocher permet aux utilisateurs d’indiquer au site de « se souvenir de moi ».
 *le site Web doit s'afficher correctement dans différents navigateurs (Firefox, Chrome). Les messages d’erreur ne doivent pas afficher des informations importantes. 
*L'utilisateur une fois déconnecté du système ou si la session utilisateur a expiré, l'utilisateur ne devrait pas pouvoir naviguer sur le site.
##Environnement :
###Navigateurs : IE, Firefox, Chrome, Safari et Opera
###Systèmes d'exploitation : Windows 11

##Règles de nommage :

Types de test : 
F:  Fonctionnel
NF : Non Fonctionnel

Fonctionnalité :
CNC : Création Nouveau Compte
CNX : Connexion au compte 
RMP : Réinitialisation de Mot de Passe 
Numéro du cas de test : 
T : Test1,2,3,4….etc. 
Exemple : 
 
Type de Tests :
Tests fonctionnels
Tests de compatibilité
Tests de sécurité
Scénarios de test :
Scénarios de tests fonctionnels:
Création de compte 
Connexion au compte
Réinitialisation de mot de passe 
Scénarios de tests de compatibilité (Non Fonctionnels) : 
Création de compte NF
Connexion au compte NF
Réinitialisation de mot de passe NF
Scénario de test pour les tests de sécurité  (Non Fonctionnels) :
Déconnexion de compte NF
Synthèse de tests  :
Tableau de tests 
Date de début : 23 Août 2024 Date de fin prévue : 02 Septembre 2024
Automatisation des tests 
Automatisation : 
Automatisation du scénario de test Création de compte sur sélénium IDE   :
Script du fichier JSON  qui contient les informations sur les tests automatisés
Capture d’écran de l'exécution de l’automatisation sur Sélénium IDE : 
    

Exportation du script en Python:
Script généré par sélénium IDE
Modifications :  
J’ai ensuite apporté des modifications au script Python généré par sélénium IDE pour améliorer la robustesse des tests: 
Script amélioré pour la robustesse des tests 


les modifications apportées: 
Ajout de Paramètres pour le navigateur : Utilisation de chrome_options avec l'argument --disable-search-engine-choice-screen pour désactiver l'écran de choix du moteur de recherche.
Méthode de Fermeture des Cookies : Ajout d'une méthode close_cookies pour gérer la fermeture automatique des bannières de cookies, évitant ainsi des interruptions dans les tests.
Mise en Pause : Introduction de la méthode pause pour insérer des délais (pauses) dans le script, permettant de gérer les temps de chargement des pages.
Utilisation de set_window_rect : Remplacement de set_window_size par set_window_rect, permettant de définir plus précisément la taille de la fenêtre.
Attente explicite avec WebDriverWait : Introduction de l'attente explicite (WebDriverWait et EC.element_to_be_clickable) pour s'assurer que les éléments sont cliquables avant de les utiliser, améliorant ainsi la fiabilité des tests.
Gestion des Exceptions : Ajout de la gestion des exceptions avec NoSuchElementException et TimeoutException pour éviter que le test ne plante en cas d'élément introuvable.
Vérifications d'Assertions : Ajout d'assertions pour vérifier que les champs de formulaire contiennent les valeurs attendues, renforçant la vérification de l'exactitude des tests.
Vérification du Contenu de la Page : Ajout d'une vérification pour s'assurer que le texte attendu est présent sur la page après certaines actions, améliorant la validation des résultats des tests.
Suppression des Actions Inutiles : Retrait des actions redondantes d'ActionChains qui étaient présentes dans le premier script, simplifiant ainsi le code.
Pytest : 
J’ai ensuite exécuté le fichier du script avec Pytest pour tester le bon fonctionnement des tests : 


Rapport HTML généré par le plugin “pytest-html”:


