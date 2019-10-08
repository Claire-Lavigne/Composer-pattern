# Utilisation du pattern

## Liste des étapes

- Récupération du repo et mise en place du projet
    - Cloner le repo `git clone...`.
    - Renommer le dossier avec le nom du projet souhaité `mv <anciennom> <nouveaunom>`
    - Se rendre dans le dossier nouvellement créé `cd <nouveaunom>`
    - Supprimer le dossier `.git` afin de ne pas écraser le repo pattern d'origine et de ne pas garder l'historique du pattern dans notre nouveau projet. `sudo rm -R .git`
    - Initialise `git` dans le dossier du projet `git init`
    
- Ouvrir repo dans VSCode `code .`
- Installation de nos dépendances avec composer `composer install`

- Création de la BDD
    - Aller sur PHPMyAdmin --> `Nouvelle base de données` --> wp_nom --> créer
- Création du fichier `wp-config.php` à partir du fichier `wp-config-sample.php`
    - Renseigner les informations de connexion à la BDD (wp_nom, claire, mdp, localhost)
    - Renseigner les clés de salage [URL pratique](https://api.wordpress.org/secret-key/1.1/salt/)
    - Renseigner la constante `WP_CONTENT_URL` avec notre url locale (http://localhost/nomsitewordpress/content)
- Changer les droits des fichiers/dossier de mon projet
    ```bash
    # user du pc et mdp du pc
    sudo chown -R <user>:www-data .
    # tout copier coller
    sudo find . -type f -exec chmod 664 {} +
    sudo find . -type d -exec chmod 775 {} +
    sudo chmod 644 .htaccess
    ```
- Se rendre sur l'url locale (localhost) de notre projet pour terminer l'installation de WordPress (fr, nomsitewordpress, root, mdp, helio...@...local, ne pas indexer)
- Se connecter
- Penser à changer l'url de la home de notre projet _(Admin BO / Réglages / Général / Adresse web du site (URL))_
    - Enlever /wp pour l'url du site
- Permalien : Titre publication
- Actualiser wordpress et tout le nécessaire
- Cliquer sur maison pour vérifier tout ok (copier coller url ds wp config)
- Extensions : installer elementor
