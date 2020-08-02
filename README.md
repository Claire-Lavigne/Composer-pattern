# Utilisation du pattern

## Liste des étapes

- Mise en place du projet
    - `git clone...`
    - `mv <anciennom> <nouveaunom>`
    - `cd <nouveaunom>`
    - `rm -Rf .git`
    - `git init`
    - `code .`
    - `composer install`

- Création de la BDD
    - Aller sur PHPMyAdmin --> `Nouvelle base de données` --> wp_nom --> créer
- Création du fichier `wp-config.php` à partir du fichier `wp-config-sample.php`
    - Renseigner les informations de connexion à la BDD
    - Renseigner les clés de salage [URL pratique](https://api.wordpress.org/secret-key/1.1/salt/)
    - Renseigner la constante `WP_CONTENT_URL` avec notre url locale
- Changer les droits des fichiers/dossier de mon projet à la racine du projet
    ```bash
    sudo chown -R <user>:www-data . (linux)
    # sudo chown -R <user>:_www . (mac)
    # to know <user> : whoami
    sudo find . -type f -exec chmod 664 {} +
    sudo find . -type d -exec chmod 775 {} +
    sudo chmod 644 .htaccess
    ```
- Se rendre sur l'url locale de notre projet pour terminer l'installation de WordPress
- Penser à changer l'url de la home de notre projet _(Admin BO / Réglages / Général / Adresse web du site (URL))_
