
# Apache

## Pages d'erreurs personnalisées

* 403 - Forbidden : Le serveur refuse de délivrer la ressource ;
* 404 - Not Found : La ressource spécifiée n'existe pas ;
* 500 - Internal Server Error : Une erreur interne au serveur est survenue.

## Installation

Définir un fichier `.htaccess` avec trois fichiers `HTML` représentant les erreurs 403, 404 et 500

```bash
  Options -Indexes
  ErrorDocument 403 /apache/error/error-403.html
  ErrorDocument 404 /apache/error/error-404.html
  ErrorDocument 500 /apache/error/error-500.html
```

**La variable `{{SITE_NAME}}` peut et doit être modifié par le nom du site.**
