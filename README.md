# Conception-des-tests-et-Automatisation-
Conception des tests pour "IT-akademy" et Automatisation avec Selenium et Pytest
# Projet de Test du Site Web d'[It-Akademy](https://inscription.it-akademy.fr/)
Création de scénarios de tests 
Types de tests appliqués 
Synthèse de tests 



[Conception des tests](https://docs.google.com/document/d/1o1g3CfSvPM0GjFFmtMKfW6YT3fQpt8lLYnLovWd1pS8/edit)





Objectif
Le projet vise à valider les fonctionnalités du site web [It-Akademy](https://inscription.it-akademy.fr/) avant la mise en production. Les principales fonctionnalités à tester sont :

Création d'un nouveau compte
Connexion à un compte existant
Réinitialisation du mot de passe
Vérification de l'affichage du site sur différents navigateurs (Firefox, Chrome)
Tester la déconnexion du compte (test de sécurité) 


L'ensemble des tests fonctionnels, de compatibilité et de sécurité a été conçu et automatisé pour vérifier l'exactitude du site d'It-Akademy dans différents environnements. Le processus d'automatisation a été amélioré pour garantir la robustesse des tests.


Types de test :
F : Fonctionnel
NF : Non Fonctionnel
Fonctionnalités :
CNC : Création Nouveau Compte
CNX : Connexion au compte
RMP : Réinitialisation de Mot de Passe
Numérotation des tests : T1, T2, T3, ...
Types de Tests
Tests Fonctionnels :
Création de compte
Connexion
Réinitialisation du mot de passe
Tests de Compatibilité (Non Fonctionnels) :
Affichage et fonctionnement sur différents navigateurs
Tests de Sécurité (Non Fonctionnels) :
Gestion de la déconnexion après expiration de session
Synthèse des Tests
Date de début : 23 Août 2024
Date de fin prévue : 02 Septembre 2024
Automatisation des Tests
Outils utilisés :
Sélénium IDE pour l'automatisation des scénarios de tests.
Script JSON généré par Sélénium pour automatiser la création de compte.
Modifications apportées au script Python généré par Sélénium IDE :
Paramètres du navigateur : Utilisation de chrome_options avec l'argument --disable-search-engine-choice-screen.
Fermeture des Cookies : Ajout d'une méthode close_cookies pour fermer les bannières de cookies automatiquement.
Mise en Pause : Ajout de pauses via la méthode pause pour gérer les temps de chargement.
Utilisation de set_window_rect : Pour un réglage précis de la taille de la fenêtre.
Attente Explicite : Introduction de WebDriverWait et EC.element_to_be_clickable pour s'assurer que les éléments sont prêts avant interaction.
Gestion des Exceptions : Ajout de la gestion des exceptions avec NoSuchElementException et TimeoutException.
Assertions et Vérifications : Ajout d'assertions pour vérifier la validité des valeurs dans les champs et le contenu des pages.
Suppression d'Actions Inutiles : Simplification du script en retirant des actions redondantes.
Exécution des Tests avec Pytest :
Les tests ont été exécutés avec Pytest pour valider le bon fonctionnement du script automatisé.
Rapport :
Génération d'un rapport HTML avec le plugin pytest-html.















