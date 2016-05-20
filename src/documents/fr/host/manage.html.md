---
title: "Gérez votre instance"
layout: "default"
category: "host"
menuOrder: 1
toc: true
---
# Gérez votre instance Cozy

## Maintenance
### Mise à jour

#### Mise à jour manuelle


Pour mettre à jour la plateforme et toutes les applications installées,
exécutez les commandes suivantes directement dans votre serveur :

```bash
sudo cozy-monitor update-all-cozy-stack
sudo cozy-monitor update-all
sudo supervisorctl restart cozy-controller
```

#### Mise à jour des applications

Pour mettre à jour une application, lancez cette commande dans votre serveur :

```bash
sudo cozy-monitor update <app>
```

### Redémarrer la pile Cozy

La pile Cozy comprend les applications Home, Proxy et Data System, c’est à dire
les applications qui permettent le fonctionnement de votre instance.

```bash
cozy-monitor restart-cozy-stack
```

### Obtenir des informations sur votre instance

Avoir la liste des applications et leur statut (allumée ou éteinte) :

```bash
cozy-monitor status
```

Afficher la version des applications de la pile :

```bash
cozy-monitor versions-stack
```

Afficher la version de toutes les applications installées :

```bash
cozy-monitor versions
```

## Gestion des applications

### Installation

Pour installer une application depuis la ligne de commande, utilisez :

```bash
sudo cozy-monitor install <app> [-r <repo>] [-d <displayName>] [-b <branch>]
```

Si l’application n’est pas maintenue par CozyCloud, il faut préciser l’adresse
de son dépôt. Vous pouvez également préciser une branche du dépôt à utiliser,
et le nom sous lequel l’application apparaitra sur la page d’accueil.


### Gestion

Pour stopper une application :

```bash
sudo cozy-monitor stop <app>
```

Pour stopper toutes les applications :

```bash
sudo cozy-monitor stop-all <app>
```

Pour démarrer une application :

```bash
sudo cozy-monitor start <app>
```

Pour redémarrer une application :

```bash
sudo cozy-monitor restart <app>
```

Pour mettre à jour une application (cela implique de cloner le dépôt Git,
exécuter `npm install` et re-démarrer l’application). Préciser l’adresse du
dépôt n’est nécessaire que pour utiliser un dépôt spécifique :

```bash
sudo cozy-monitor update <app> [repo]
```

Mettre à jour toutes les applications installées :

```bash
sudo cozy-monitor update-all
```


### Désinstallation

Pour désinstaller une application, tapez simplement :

```bash
sudo cozy-monitor uninstall <app>
```

## Gestion de la base de données

Par défaut, le nom de la base de données utilisée par ces commandes est `cozy`.

Pour compresser la base (en supprimant les versions non utilisées des documents) :

```bash
sudo cozy-monitor compact [database]
```

Compresser une vue CouchDB spécifique :

```bash
sudo cozy-monitor compact-views <view> [database]
```

Compresser toutes les vues :

```bash
sudo cozy-monitor compact-all-views [database]
```

Faire une sauvegarde de la base en la répliquant sur une autre instance CouchDB :

```bash
sudo cozy-monitor backup [target]
```

Nettoyer la base de données :

```bash
sudo cozy-monitor cleanup [database]
```

## Commandes diverses

Recharger toutes les routes du Proxy applicatif à partir du système de données :

```bash
sudo cozy-monitor reset-proxy
```

## Augmenter l’espace disque

Toutes les données et les fichiers sont stockés dans CouchDB.  Le moyen le plus
simple d’allouer plus d’espace disque à votre instance est de modifier la
configuration de CouchDB.  Actuellement, les données sont enregistrées dans le
dossier :

```bash
/usr/local/var/lib/couchdb/
```

Ce chemin peut aussi être `/var/lib/couchdb`, notamment si vous avez installé
cozy sur une Debian ou une Ubuntu.

Vous pouvez modifier ce chemin, par exemple pour le faire pointer vers un autre
disque avec plus d’espace libre.  Pour cela, éditez le fichier :

```bash
/usr/local/etc/couchdb/local.ini
```

C'est le fichier `/etc/couchdb/local.ini` sur Debian et Ubuntu.

Ajoutez une section couchdb si elle n’es pas déjà présente. Vous pouvez alors
modifier le paramètre spécifiant le dossier où est stocké la base de données :

```bash
[couchdb]
database_dir = /home/storage/cozy-data
view_index_dir = /home/storage/cozy-data
```

Ceci fait, il faut couper CouchDB, déplacer le fichier contenant la base, puis
la relancer (en tant que root) :

```bash
service couchdb stop
mkdir /home/storage/cozy-data/
# cp here, to have a copy of the data in case of problem.
cp /usr/local/var/lib/couchdb/* /home/storage/cozy-data/
chown -R couchdb:couchdb /home/storage/cozy-data/ # Rights required.
service couchdb start
```

Pour Debian et Ubuntu, le redémarrage de Couchdb ne passe pas supervisord :

```bash
service couchdb stop
mkdir /home/storage/cozy-data/
# cp here, to have a copy of the data in case of problem.
cp /var/lib/couchdb/* /home/storage/cozy-data/
chown -R couchdb:couchdb /home/storage/cozy-data/ # Rights required.
service couchdb start
```

**Il est fortement recommandé de sauvegarder vos données avant une telle
opération** Vous pouvez soit faire une sauvegarde des fichiers contenant la
base, soit répliquer la base sur une autre instance CouchDB.


## Utiliser un certificat Let’s Encrypt

Vous pouvez vous référer à [cet article](https://blog.cozycloud.cc/post/2016/01/06/Un-certificat-Let-s-Encrypt-pour-votre-Cozy) sur notre blog pour découvrir comment générer, installer et renouveler automatiquement un certificat gratuit sur votre serveur grâce à Let’s Encrypt.


## Divers

### Augmenter la taille maximale des fichiers téléversés.

Si vous utilisez Nginx comme serveur proxy inverse, il vous sera impossible de téléverser de gros fichiers. Nginx limite par défaut la taille des requêtes envoyées par les clients à 1Mo. Pour augmenter cette limite, ajoutez simplement une instruction [client_max_body_size](http://nginx.org/en/docs/http/ngx_http_core_module.html#client_max_body_size) à votre configuration Nginx.

