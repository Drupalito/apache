
# Apache

## Pages d'erreurs personnalisées

* 403 - Forbidden : Le serveur refuse de délivrer la ressource ;
* 404 - Not Found : La ressource spécifiée n'existe pas ;
* 500 - Internal Server Error : Une erreur interne au serveur est survenue.

[Voir la liste exhaustive des codes HTTP](https://fr.wikipedia.org/wiki/Liste_des_codes_HTTP)

## Installation

1. Dans le fichier `vhost`, définir les trois fichiers `HTML` ;
2. Le fichier index.html servira d'affichage par défault ;
3. **La variable `{{ SITE_NAME }}`, contenu dans les `.html` peut et doit être modifié par le nom du site.**.

```bash
  <VirtualHost *:80>
    # 1.
    DirectoryIndex home.html index.html

    # 2.
    ErrorDocument 403 /apache/error/error-403.html
    ErrorDocument 404 /apache/error/error-404.html
    ErrorDocument 500 /apache/error/error-500.html
    ErrorDocument 501 /apache/error/error-500.html
    ErrorDocument 502 /apache/error/error-500.html
    ErrorDocument 503 /apache/error/error-500.html
    ErrorDocument 504 /apache/error/error-500.html
  </VirtualHost>
```
