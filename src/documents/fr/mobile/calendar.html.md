---
title: "Agendas"
layout: "default"
category: "mobile"
menuOrder: 2
toc: true
---

# Agendas

## Préparer votre Cozy
Cozy utilise CalDAV, qui est le protocole standard, pour synchroniser vos agendas sur tous vos périphériques. Tout est géré dans une application spécifique, Sync.

* Premièrement, allez dans votre Cozy dans le menu "Choisissez vos apps".
* Puis sélectionnez l'application "Sync".
* Acceptez les permissions de l'application et attendez la fin de l'installation.

<center>![Sync's installation intructions](/assets/images/mobile/install_sync_steps.gif)</center>

<br />
<br />
* Après ça, vous devez récupérer vos identifiants CalDAV.
* Ouvrez l'application Sync.
* Notez le mot de passe.

<center>![Get CardDav credentials intructions](/assets/images/mobile/use_sync_steps.gif)</center>

<br />
<br />
Vous êtes maintenant prêt à synchroniser vos périphériques !

Consultez la section correspondant au système de votre périphérique pour continuer.
## Android

Pour Android, nous vous conseillons d'utiliser directment l'[application Cozy](/fr/mobile/files.html) sous Android.


#### Installation

Sur Android, plusieurs applications permettent de synchroniser votre calendrier. Nous vous conseillons d’utiliser [DavDroid](http://davdroid.bitfire.at/) qui est un logiciel libre (l’application est payante dans le PlayStore de Google, vous pouvez également la télécharger et l’installer gratuitement dans le [F-droid store](https://f-droid.org/repository/browse/?fdid=at.bitfire.davdroid)).

#### Configuration
Une fois l'application installée, ouvrez-là et cliquez sur le bouton pour créer un nouveau compte (suivez le cercle bleu dans l'image ci-dessous).
<center>![Android step 1](/assets/images/mobile/android/step1.png)</center>

<br />
<br />
Puis, sélectionnez "DavDroid".
<center>![Android step 2](/assets/images/mobile/android/step2.png)</center>

<br />
<br />
Vous aurez deux choix. Choisissez "Connexion avec URL et identifiants".
<center>![Android step 3](/assets/images/mobile/android/step3.png)</center>

<br />
<br />
Remplissez le formulaire avec les identifiants que vous avez notés lors de l'étape 1.
<center>![Android step 4](/assets/images/mobile/android/step4.png)</center>

<br />
<br />
Sélectionnez les agendas que vous voulez synchroniser. Si vous voulez aussi synchroniser vos contacts, sélectionnez le carnet d'adresses au même moment.
<center>![Android step 5](/assets/images/mobile/android/step5.png)</center>

<br />
<br />
Choisissez un nom pour votre compte, "Cozy" fera très bien l'affaire.
<center>![Android step 6](/assets/images/mobile/android/step6.png)</center>

<br />
<br />
Vous avez terminé, mais si vous voulez forcer la première synchronisation, allez dans la liste des comptes.
<center>![Android step 7](/assets/images/mobile/android/step7.png)</center>

<br />
<br />
Sélectionnez le compte DavDroid dans la liste.
<center>![Android step 8](/assets/images/mobile/android/step8.png)</center>

<br />
<br />
Touchez le bouton "Calendar", ce qui aura pour effet de démarrer une synchronisation.
<center>![Android step 9](/assets/images/mobile/android/step9.png)</center>

<br />
<br />
Félicitations, votre périphérique mobile est maintenant synchronisé avec votre Cozy !

## iOS

#### Configurez votre compte CalDAV

Ouvre les options, sélectionnez "Email, Contacts, Agendas" et cliquez sur "Ajouter un compte" :
<center>![iOS step 1](/assets/images/mobile/ios/contacts/step1.jpg)</center>

<br />
<br />
Puis sélectionnez "Autre compte" :
<center>![iOS step 2](/assets/images/mobile/ios/contacts/step2.jpg)</center>

<br />
<br />
Sélectionnez ensuite "Ajouter un compte CalDAV" dans la section Contacts :
<center>![iOS step 3](/assets/images/mobile/ios/contacts/step3.jpg)</center>

<br />
<br />
Enfin, remplissez le formulaire avec les identifiants que vous avez notés lors de l'étape 1 :

* le champ "Serveur" va changer pour chaque utilisateur : adresse-de-votre-cozy/public/sync/principals/me ;
* le champ "Nom d'utilisateur" sera toujours "me" ;
* le champ "Mot de passe" sera celui que vous avez noté ;
* le champ "Description" permet de choisir un nom pour identifier ce compte. "Cozy" fera très bien l'affaire.

<center>![iOS step 4](/assets/images/mobile/ios/calendar/step4.jpg)</center>

<br />
<br />
Puis cliquez sur suivante, configurez les alarmes, et enregistrez vos choix.
<center>![iOS step 5](/assets/images/mobile/ios/calendar/step5.jpg)</center>

<br />
<br />
Félicitations, votre périphérique mobile est maintenant synchronisé avec votre Cozy !
Vous pouvez à présent configurer l'application mobile Agenda pour choisir quels agendas afficher.

#### Configurer vos agendas

Ouvrez l'application Calendar sur votre terminal mobile.

Vous pouvez déjà visualiser les agendas de votre Cozy. Cliquez sur les agendas pour les rendre visibles ou invisibles.
<center>![iOS step 6](/assets/images/mobile/ios/calendar/step6.jpg)</center>

<br />
<br />
Ouvrez le menu et cliquez sur le bouton pour ajouter un nouveau calendrier.
<center>![iOS step 7](/assets/images/mobile/ios/calendar/step7.jpg)</center>

<br />
C'est tout ! Vous pouvez gérer vos événements sur votre mobile ou sur votre Cozy de façon transparente.

## OSX

Dans l'application Calendrier, cliquez sur "Calendrier", puis sur "Ajouter un compte" :
<center>![OSX step 1](/assets/images/mobile/osx/calendar/step1.jpg)</center>

<br />
<br />
Sélectionnez ensuite "Ajouter un compte CalDAV..." et cliquez sur "Continuez" :
<center>![OSX step 2](/assets/images/mobile/osx/calendar/step2.jpg)</center>

<br />
<br />
Sélectionnez le Type de contact : Manuel.
Enfin, remplissez le formulaire avec les identifiants que vous avez notés lors de l'étape 1 :

* le champ "Serveur" va changer pour chaque utilisateur : adresse-de-votre-cozy/public/sync/principals/me ;
* le champ "Nom d'utilisateur" sera toujours "me" ;
* le champ "Mot de passe" sera celui que vous avez noté ;

<center>![OSX step 3](/assets/images/mobile/osx/calendar/step3.jpg)</center>

<br />
<br />
Puis cliquez sur créer.
Félicitations, votre ordinateur est maintenant synchronisé avec votre Cozy !
Vous pouvez à présent configurer l'application Calendrier pour choisir quels agendas afficher.
C'est tout ! Vous pouvez gérer vos événements sur votre ordinateur ou sur votre Cozy de façon transparente.

## Firefox OS

#### Installation

Il n'y a rien à installer pour commencer avec Firefox OS ! Ouvrez simplement l'application "Calendar".

#### Configuration

Ouvrez le menu et cliquez sur le bouton pour ajouter un nouveau calendrier.
<center>![Firefox OS step 1](/assets/images/mobile/firefoxos/step1.png)</center>

<br />
<br />
Puis choisissez l'option "CalDAV" dans le menu.
<center>![Firefox OS step 2](/assets/images/mobile/firefoxos/step2.png)</center>

<br />
<br />
Enfin, remplissez le formulaire avec les identifiants que vous avez notés dans l'étape 1 :

* le premier champ sera toujours "me" ;
* le second sera le mot de passe que vous avez noté précédemment ;
* le troisième change pour chaque utilisateur : https://adresse-de-votre-cozy/public/sync/principals/me

<center>![Firefox OS step 3](/assets/images/mobile/firefoxos/step3.png)</center>

<br />
<br />
C'est tout ! Vos agendas seront synchronisés régulièrement (par défaut toutes les 15 minutes). Vous pouvez sélectionner les calendriers que vous voulez synchroniser directement depuis le menu.
<center>![Firefox OS step 4](/assets/images/mobile/firefoxos/step4.png)</center>

<br />
<br />
Félicitations, votre périphérique mobile est synchronisé avec votre Cozy !

## Thunderbird (Windows, OSX et GNU/Linux)

#### Installation

Il est nécessaire d'installer le module complémentaire Lightning  : https://addons.mozilla.org/fr/thunderbird/addon/lightning/

#### Configurez votre compte CalDAV

Dans "Fichier", sélectionnez "Nouveau", et "Agenda...".
<center>![thunderbird step 1](/assets/images/mobile/thunderbird/fr/calendar/step1.jpg)</center>

<br />
<br />
Sélectionnez "Sur le réseau" et cliquez sur "suivant".
<center>![thunderbird step 2](/assets/images/mobile/thunderbird/fr/calendar/step2.jpg)</center>

<br />
<br />
Sélectionnez CalDAV et entrez l'adresse d'emplacement de votre agenda (dans Cozy) ; elle est différente pour chaque utilisateur et chaque agenda : https://adresse-de-votre-cozy/public/sync/calendars/me/nom-de-votre-agenda (attention aux majuscules du "nom-de-votre-agenda").
Cochez "Prise en charge du mode hors connexion" si vous souhaitez que Thunderbird mémorise les évènements pour que vous puissiez les conulter sans accès à internet.
Cliquez sur "suivant".
<center>![thunderbird step 3](/assets/images/mobile/thunderbird/fr/calendar/step3.jpg)</center>

<br />
<br />
Entrez un nom pour identifier cet agenda. Il est conseillé d'utiliser le même nom que celui de votre Cozy, avec le suffixe cozy : "nom-de-votre-agenda_cozy".
Choisissez une couleur (la même que celle de votre agenda dans cozy est conseillée). Choisissez aussi si vous souhaitez afficher les alarmes de cet agenda, et enfin, sélectionnez l'adresse de courriel en lien avec l'activité de cet agenda.
Cliquez sur "suivant".
<center>![thunderbird step 4](/assets/images/mobile/thunderbird/fr/calendar/step4.jpg)</center>

<br />
<br />
Cliquez sur "Terminer". Votre agenda est bien créé dans Thunderbird.

#### Première synchronisation

Lorsque Thunderbird va vouloir synchroniser votre agenda pour la première fois, il va vous demander vos identifiants.
* le champ "Utilisateur" sera toujours "me" ;
* le champ "Mot de passe" sera celui que vous avez noté ;
* Cochez la case "Utiliser le gestionnaire de mots de passe pour se souvenir de ce mot de passe" afin de ne plus avoir à le renseigner à chaque synchronisation.
<center>![thunderbird step 5](/assets/images/mobile/thunderbird/fr/calendar/step5.jpg)</center>

<br />
<br />

Félicitations, votre ordinateur est maintenant synchronisé avec votre Cozy !
C'est tout ! Vous pouvez gérer vos événements sur votre ordinateur ou sur votre Cozy de façon transparente.


<br />
<br />


#### Comment synchroniser un agenda existant

Synchroniser un agenda déjà créé dans Thunderbird avec votre serveur Cozy demande quelques manipulations. Il faut créer un nouvel agenda dans Cozy, y importer votre agenda local, puis créer un nouvel agenda local synchronisé avec le serveur.

Voici comment faire depuis Thunderbird :

* **étape 1 : exporter votre agenda actuel depuis Thunderbird/Lightning** : dans l’onglet agenda de Thunderbird, dans la colonne de gauche "agendas" cochez la case correspondant à l’agenda et faites un clic droit > exporter. Notez bien l’emplacement où votre ficher .ics est sauvegardé ;

* **étape 2 : créer un nouvel agenda dans votre Cozy** : si vous ne l’avez pas encore fait, installez l’application Calendar.  Ouvrez l’application et cliquez sur le "+" pour ajouter un agenda. En bas à gauche cliquez sur « Sync settings ». Dans la fenêtre qui s’ouvre, allez dans la section « Importer un iCalendar » et cliquez sur le bouton « sélectionner un fichier iCalendar ». Sélectionnez votre fichier .ics précédemment créé.  Attention si votre calendrier comporte beaucoup d’événements l’importation risque d’être un peu longue ;

* **étape 3 : récupérer l’url de synchronisation** : dans votre Cozy, lancez l’application Sync et dans la section « Configuration de CalDAV (Agenda) » cliquez sur « Thunderbird (Lightning) ». Sélectionnez l’agenda que vous voulez synchroniser et copiez l’url indiquée dans la boite en-dessous ;

* **étape 4 : Créer un agenda synchronisé dans Thunderbird (Lightning)** : il vous reste à retourner dans Thunderbird, créer un nouvel agenda et le synchroniser avec l’url précédente, comme expliqué ci-dessus. Vous pouvez alors supprimer l’agenda initial, non synchronisé, pour ne pas avoir de doublons.


<br />
<br />


## Ressources connectées

* [Discussion sur le forum](https://forum.cozy.io/)

