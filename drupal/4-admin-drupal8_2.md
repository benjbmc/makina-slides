
# Objectifs de la formation - Les fonctionnalités avancées

  * __Administration (Tâches d'administration, Mises à jour, sauvegarde, Multi-sites, performance)__
  * Référencement (urls, meta-tags, sitemap.xml)
  * Multilinguisme
  * Autres contenus (médias, newsletters, formulaires)
  * Recherche
  * "Outside-In"

.fx: progress

--------------------------------------------------------------------------------

# Tâches d'administration

  * _Configurer > Personnes_ : Paramétrage/blocage de comptes (module _Ban_)
  * _Configurer > Système_ : Informations et Cron
  * _Configurer > Développement_ : Erreurs et Maintenance
  * _Rapports > Rapport d'état_ : monitorer son site
  * _Rapports > Erreurs récentes_ : monitorer son site
  * _Rapports > Statistiques_ : Module _Statistics_ du cœur (mais il ne couvre pas
  ce qu'attendent les gens, préférer _Google Analytics_)

![][4]

--------------------------------------------------------------------------------

# Mises à jour

  * Rapport > Mises à jour disponibles (module _Update manager_)

# ATTENTION : Toujours faire une sauvegarde des fichiers et de la base de données de façon préalable.

![][1]

--------------------------------------------------------------------------------

# Mises à jour des modules

  * Télécharger la nouvelle version
  * Supprimer l'ancienne version
  * Ajouter la nouvelle version
  * Aller dans « Rapports > tableau de bord »
  * Repérer la ligne "Mise à jour de la base de données"
  * Si une mise à jour est nécessaire suite aux modifications, un lien
apparait.
  * Cliquez sur le lien et suivre les instructions

--------------------------------------------------------------------------------

# Mises à jour du cœur

  * Instructions sur <https://www.drupal.org/node/2700999>
  * Mettre le site en mode "maintenance"
  * Supprimer les fichiers dans /code, /vendor, et à la racine du site
  * Remplacer par les nouveaux fichiers
  * Décompresser la nouvelle version du cœur

--------------------------------------------------------------------------------

# DRUpal SHell

  * [https://github.com/drush-ops/drush][2]

  * Exécution d'installation et de mise à jour en ligne de commande
    * gain de temps
    * administration simplifiée
    * nombreuses commandes et support par les modules

  * Liste des commandes : [https://drushcommands.com/][3]

  * Disponible sous Linux

  * Relativement supporté sur Windows (pour Drupal 8, installer avec Composer)
  
--------------------------------------------------------------------------------

# Drupal Console

  * [https://drupalconsole.com/][48]

  * Inspiré de la Symfony Console

  * Liste des commandes : *drupal list*
    * drupal list | grep grenerate (liste les commandes ne concernant que *generate*)
    
  * Disponible sous Linux / Windows / MacOS
  
  * Version 1.0.0-rc10
  
  * plus de 300 000 téléchargements
  
--------------------------------------------------------------------------------

# Drupal Console VS Drush

  * Concurrents ou compléments ? Fusion ?
  
![][49]

--------------------------------------------------------------------------------

# Drupal CMI

  * Configuration Migration Interface
  
  * Configuration > Configuration synchronization
  
  * Export global : *pas conseillé*
  
  * Export au détail : Blocs, Types de contenus, Champs, Rôles ...
  
  * Fichiers yml
  
  * Remplace le module Features ...
    
![][50]

--------------------------------------------------------------------------------

# Sauvegardes

  * Module _Backup & Migrate_
    * Sauvegarde de la base de données
    * Sauvegarde des fichiers
    * Pas encore stable pour D8

  * Script shell maison

  * Commandes drush
    * drush archive-dump
    * drush archive-restore
    * drush sql-dump
    * drush sql-client

--------------------------------------------------------------------------------

# Installation multi-sites

  * Traditionnel - Partage des modules
    * Décompresser Drupal
    * Créer les répertoires dans /sites/ avec les noms des domaines
    * Copier le contenu de /sites/default dans les sous-répertoires.
    * Lancer l'installation classique via le navigateur

  * Module Domain access (en cours de port D8) - Partage des données
    * Basé sur 1 instance (même base de données,  même code)
    * Facilité d'administration
    * Partage de contenus, utilisateurs, blocks, etc.

  * [https://www.palantir.net/blog/multi-headed-drupal][23]

--------------------------------------------------------------------------------

# Performance

  * Cache activé par défaut
    * Fonctionne très bien pour les anonymes

  * Intégration Varnish, Redis, Memcache, CDN, etc.

  * Passez à PHP7 et MySQL 5.6 !

--------------------------------------------------------------------------------

# Objectifs de la formation - Les fonctionnalités avancées

  * Administration (Tâches d'administration, Mises à jour,  sauvegarde,
Multi-sites, performance)
  * __Référencement (urls, meta-tags, sitemap.xml)__
  * Multilinguisme
  * Autres contenus (médias, newsletters, formulaires)
  * Recherche
  * "Outside-In"

.fx: progress

--------------------------------------------------------------------------------

# Ré-écriture des urls

  * Module path (core) et __Pathauto__
  * Recherche et métadonnées > Alias d'urls
  * Gestion de la ré-écriture automatique
    * Selon les types de contenu
    * Selon la taxonomie
  * Régénération d'urls en batch
  * Création à partir de tokens

--------------------------------------------------------------------------------

# Module Token

  * Sorte de variables affichant certaines données en fonction d'un contexte
  * Global
    * nom du site
    * date actuelle
  * Node
    * titre
    * champs
    * date
  * Utilisateur
    * nom d'utilisateur
    * date de dernière connexion

Et bien d'autres

--------------------------------------------------------------------------------

# Module Metatag

  * Méta-données intégrées dans le code HTML des pages du site
  * à définir pour chaque contenu
  * paramétrage pour la page d'accueil
  * possibilité d'ajouter de nombreux tag

--------------------------------------------------------------------------------

# Module Simple XML Sitemap

  * Génération d'un fichier sitemap.xml à la racine avec les urls du site (parsing par les robots de référencement)
  * Paramétrage pour définir quelles pages sont à inclure / exclure
  * Reconstruction automatique au lancement du cron

![][5]

--------------------------------------------------------------------------------

# Autres modules

## Module Google Analytics

  * Code à renseigner, script ajouté à toutes les pages

## Sémantique

  * Metadonnées pour l'affichage dans les résultats de recherche
  * Inclus dans le cœur de Drupal (module RDF)

## Redirect

  * Gestion des redirections

--------------------------------------------------------------------------------

# Objectifs de la formation - Les fonctionnalités avancées

  * Administration (Tâches d'administration, Mises à jour,  sauvegarde,
Multi-sites, performance)
  * Référencement (urls, meta-tags, sitemap.xml)
  * __Multilinguisme__
  * Autres contenus (médias, newsletters, formulaires)
  * Recherche
  * "Outside-In"

.fx: progress

--------------------------------------------------------------------------------

# Le multilinguisme

  * 4 modules présents dans le coeur
    * Language (gestion des langues du site)
    * Interface Translation (interface de traduction, administration du site en FR)
    * Configuration Translation (traduction de la configuration)
    * Content Translation (traduction du contenu)

![][14]
    
--------------------------------------------------------------------------------

# La langue

  * Ajout de langage
  * Gère également si la langue s'écrit de gauche à droite

![][15]
    
--------------------------------------------------------------------------------

# La langue

  * Activé automatiquement si on choisit l'installation dans une autre langue
  * Permet de combiner différentes méthodes de détection de langue

![][16]
    
--------------------------------------------------------------------------------

# Traduction de l'interface

  * Interface de traduction du back-office

![][17]
 
![][18]

--------------------------------------------------------------------------------

# Traduction du contenu

  * Module "Content Translation"
  * "Contenu" = 
    * Nœuds
    * Blocs
    * Menus
    * Taxonomie
    * Utilisateurs
 
![][19]

--------------------------------------------------------------------------------

# Traduction du contenu

  * Activation du multilinguisme sur le type de contenu
    * (ou utilisateur, vocabulaire, ...)
  * Stratégie de langage par défaut (selon les profils, droits, ...)

![][20]

--------------------------------------------------------------------------------

# Traduction du contenu

  * Onglet "Traduire" pour chaque contenu
    * Tableau de synthèse du statut de traduction pour toutes les langues
    * Ajout d'une traduction par langue

![][6]

--------------------------------------------------------------------------------

# Traduction du contenu

  * Attention, il faut paramétrer les champs qui peuvent se traduire !
  * Administration > Configuration > Langue et région > Langue du contenu et traduction

![][21]

--------------------------------------------------------------------------------

# Traduire les blocs

  * Pour chaque bloc dans l'onglet ''Configurer le bloc''
    * Restriction du bloc à certains langages

![][7]

--------------------------------------------------------------------------------

# Traduire la configuration

![][8]

  * Tout le reste du site...
  * Page d'accueil, 404, ...
  * Administration > Configuration > Langue et région > Traduction de la configuration

![][22]

--------------------------------------------------------------------------------

# Traduire les menus

  * 2 stratégies :
    * Créer un menu par langue
    * Traduire un menu, qui comprendra alors des éléments de chaque langue (pas tous affichés)

--------------------------------------------------------------------------------

# Objectifs de la formation - Les fonctionnalités avancées

  * Administration (Mises à jour, Multi-sites, sauvegarde, cron,
performance, architecture)
  * Référencement (urls, meta-tags, sitemap.xml)
  * Multilinguisme
  * __Autres contenus (médias, newsletters, formulaires)__
  * Recherche
  * "Outside-In"

.fx: progress

--------------------------------------------------------------------------------

# Gestion des médias 

  * Depuis Drupal 8.4
    * Media API dans le coeur (stable)
    
  * Utilisation avec Embed et Entity browser
    * Gestionnaire de fichiers (Files/ Images)
    * Intégration au WYSIWYG
 
![][51]
![][52]
    
--------------------------------------------------------------------------------

# Gestion des médias 

  * Media Initiative
    * <http://www.drupalmedia.org>
    * Suite de modules (DropzoneJS, Media entity video ...)
    * Fichiers image, vidéo, audio, ...
    * La plupart des modules sont en version 1.x
    
![][26]

--------------------------------------------------------------------------------

# Newsletter

  * Module Simplenews
    * Gestion des abonnements
    * Gestion des envois instantanés ou asynchrones
    * Gestion de plusieurs catégories de newsletters
    * Pas tout à fait finalisé pour Drupal 8

  * Gestion des souscriptions seules
    * Service externe : _Mailchimp_ (ou d'autres, Mailjet, ...)
    * Solution recommandée aujourd'hui

--------------------------------------------------------------------------------

# Formulaires

  * Référence Drupal : module Webform
    * YAML Form Jusqu'en Novembre 2016
    * Création/Gestion intuitive des champs
    * Visualisation/export des soumissions
  * Utilisation du module __Contact__
    * Avec Contact Storage (voir <http://flocondetoile.fr/blog/drupal-8-injecter-un-formulaire-de-contact-dans-un-contenu-en-5-etapes>)
    * et d'autres éventuellement (pour l'export CSV)
    

--------------------------------------------------------------------------------

# Formulaires

  * Utilisation du module __Webform__
       * Module le plus complet à ce jour
       * Version actuelle suffisament stable
       * Pack de plusieurs modules
       
![][44]

--------------------------------------------------------------------------------

# Formulaires

  * __Webform__
       * Création -> utilisation de fichiers YML
       
![][45]

--------------------------------------------------------------------------------

# Formulaires

  * __Webform__
       * Activation de Webform UI
       * Editeur visuel
       
![][46]

--------------------------------------------------------------------------------

# Formulaires

  * __Webform__
       * Nombreux choix de configuration
       * Gestion des droits par groupes/utilisateurs
       * Configuration des emails
       * Consultation/EXport des soumissions
       
![][47]

--------------------------------------------------------------------------------

# Objectifs de la formation - Les fonctionnalités avancées

  * Multilinguisme
  * Administration (Mises à jour, Multi-sites, sauvegarde, cron,
performance, architecture)
  * Référencement (urls, meta-tags, sitemap.xml)
  * Autres contenus (médias, newsletters, formulaires, modération)
  * __Recherche__
  * "Outside-In"


.fx: progress

--------------------------------------------------------------------------------

# La recherche

  * Search API
    * Apache Solr (module __Search API Solr Search__)
    * ElasticSearch (module __Elasticsearch Connector__)
  * Gestion des facets, des fichiers, ...

--------------------------------------------------------------------------------

# "Outside-In"

  * Utilisation de fonctionnalités d'administration depuis le "Front-end"
  
![][40]

--------------------------------------------------------------------------------

# "Outside-In"

  * Edtition en "live"
    * Nom du site, slogan
    * Noms / liens des menus
    * ...
    
![][41]

--------------------------------------------------------------------------------

# "Outside-In"

  * Positionner des blocs
    * Affichage, selection de la région
    
![][42]

--------------------------------------------------------------------------------

# "Outside-In"

  * Positionner des blocs
    * Selection du bloc
    
![][43]

--------------------------------------------------------------------------------

# La roadmap de Drupal

  * <https://www.drupal.org/core/roadmap>
  * Aujourd'hui :
    * Media
    * Workflow
  * Dans le futur :
    * CMI 2.0
    * Back-office en JS
    * Mises à jour automatiques
  * Peut-être :
    * Modèle de données
    * Cross-channel
    
![][24]

--------------------------------------------------------------------------------

# Drupal 9

![][53]

<https://dri.es/plan-for-drupal-9>


--------------------------------------------------------------------------------

# Mise production d'un site Drupal

Transférer fichiers et données

Pour le passage en production

  * Attention au fichier settings.php, services.yml
  * Pathologic pour réparer les chemins cassés
  * <https://microserve.io/blogs/drupal-go-live-checklist-revisited>

Pour le développement

  * Stage File Proxy
  * Désactiver les mails _Reroute Email_
  * Se faire passer pour un utilisateur _Masquerade_
  * Une URL à connaître : /core/rebuild.php (vide les caches)

--------------------------------------------------------------------------------

# Procédure de construction d'un site

  * Configuration initiale (multilinguisme, workflow, metatag, ...)
  * Formats d'images, directement à partir des maquettes
  * Types de contenu
  * Views
  * Mise en page (blocs, panels ou display suite ou ...)
  * Intégration graphique
  * Développements spécifiques ou modules additionnels (flags, rules, ...)

  * __Problème__ : aucune intégration graphique avant la fin => incompatible avec une livraison régulière...

  * <https://makina-corpus.com/blog/metier/2016/comment-creer-un-site-web-avec-drupal>

--------------------------------------------------------------------------------

# Procédure de construction d'un site

  * Configuration initiale => style guide, charte graphique par défaut
  * Formats d'images
  * Types de contenu => templates de contenu
  * Views => templates de Views
  * Mise en page => finition du template
  * Développements spécifiques ou modules additionnels (flags, rules, ...)
  * Intégration graphique des derniers modules

--------------------------------------------------------------------------------

# Quelques exercices pour terminer : les contenus

  * Créer un  article
  * Le modifier en créant une révision
  * Modifier son résumé pour la page d'accueil
  * Créer une page à l'URL "/a-propos"
  * Créer un article sans le publier
  * Le publier en modifiant la date de publication à hier
  * Retirer tous les articles déjà écrits de la page d'accueil
  * Changer les paramètres d'article pour que les révisions se créent par défaut
  * Poster quelques commentaires sur le site, les retirer, tout en ajoutant
  la page de gestion des commentaires dans les raccourcis

--------------------------------------------------------------------------------

# Quelques exercices pour terminer : les utilisateurs

  * Créer un compte utilisateur "communication"
  * Modifier ce compte pour lui mettre comme mot de passe "toto"
  * Créer un rôle "webmaster" et affecter l'utilisateur "communication"

--------------------------------------------------------------------------------

# Quelques exercices pour terminer : les blocs

  * Mettre le bloc des derniers commentaires en haut de la barre de gauche
  * Mettre le bloc indiquant les utilisateurs actuels sur le site sur la barre
  de droite, uniquement pour les administrateurs
  * Créer un bloc "Bienvenue sur le site" et ne l'affiche que sur la page
  d'accueil (au-dessus du contenu)
  * Supprimer le titre du bloc "Navigation"
  * Déplacer le bloc de recherche dans la zone d'en-tête

--------------------------------------------------------------------------------

# Quelques exercices pour terminer : les menus

  * Créer un lien vers le blog de ma société (http://makina-corpus.com/blog)
  dans le menu principal
  * Ajouter le lien vers la page "à propos" dans le menu du pied de page
  * Créer un tag "important", tagger quelques contenus, et mettre un lien dans
  le menu principal vers la page de taxonomy
  * Mettre les liens "Créer une page", "Créer un article" visibles en permanence
  (dépliés dans le menu)

--------------------------------------------------------------------------------

# Quelques exercices pour terminer : le bonus

  * Modifier le format de text "Filtered HTML" pour que les H2, H3, H4 puissent être acceptés
  * Changer le nom du site
  * Changer le texte de la page 404

--------------------------------------------------------------------------------

# Questions ?


   [1]: img/update8.png

   [2]: https://github.com/drush-ops/drush

   [3]: https://drushcommands.com/

   [4]: img/reports8.png

   [5]: img/sitemap.png

   [6]: img/traduction.png

   [7]: img/block_translation.png

   [8]: img/configuration_translation.png

   [9]: img/panel.png

   [10]: img/panel2.png

   [11]: img/media.png

   [12]: img/webform.png

   [13]: img/export_webform.png

   [14]: img/multilinguisme.png

   [15]: img/add_language.png

   [16]: img/language_detection.png

   [17]: img/interface_translation.png

   [18]: img/user_interface_translation.png

   [19]: img/content_translation.png

   [20]: img/content_type_translation.png

   [21]: img/language_field_translation.png

   [22]: img/system_information_translation.png

   [23]: https://www.palantir.net/blog/multi-headed-drupal

   [24]: img/original_release_schedule.png
   
   [26]: img/media_entity.png
      
   [40]: img/outside_in.png
   
   [41]: img/outside_in_2.png

   [42]: img/outside_in_3.png

   [43]: img/outside_in_4.png

   [44]: img/webform-d8.png
   
   [45]: img/webform-d8-2.png
   
   [46]: img/webform-d8-3.png
   
   [47]: img/webform-d8-4.png

   [48]: https://drupalconsole.com
   
   [49]: img/drush-dc.png
   
   [50]: img/cmi.png
   
   [51]: img/media_d8_1.png
   
   [52]: img/media_d8_2.png

   [53]: img/Drupal9_release_plan.jpg
