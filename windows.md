---
layout: default
title: 13. Interopérabilité avec Microsoft Windows - Utiliser openSUSE dans un réseau Windows, gestion de documents et exécution d'applications Windows
permalink: windows
---

# 13. Interopérabilité MS Windows

Le monde des PC est dominé par Microsoft, lesquels ne sont particulièrement connus pour faciliter l'interopérabilité. Malgré cela, il est possible d'interagir avec leurs OS sans accros dans la plupart des cas. Ce chapitre présente des moyens de résolution des problèmes courants.

## 13.1 Documents Office

LibreOffice utilise par défaut le format Open Document (\*.odt, \*.ods, \*.odp, etc.) qui est un standard ouvert. Ce format est pris en charge, en partie, par Microsoft Office à compter de la version 2007 Service Pack 2. Vous pouvez également suggérer à vos contacts utilisants MS Windows et Mac OSX d'installer LibreOffice, celui-ci étant aussi libre et gratuit sur ces plateformes.

LibreOffice peut aussi lire et écrire avec de bons résultats les formats de fichiers Microsoft Office (\*.doc, \*.xls, \*.ppt, \*.docx, \*.xlsx, \*.pptx etc.) ainsi qu'une variété d'autres formats.

{% include tip.html tip="Si vous tombez sur certains documents Microsoft que LibreOffice ne parvient pas interprêter correctement, pensez à tester avec la suite Calligra, vous obtiendez peut-être de meilleurs résultats." %}

## 13.2 Réseau Windows

Pour partager des ressources avec des machines MS Windows sur un réseau local, on utilise le service Samba.

### 13.2.1 Accéder aux partages

Aucune configuration n'est requise pour accéder aux fichiers partagés par d'autres. Il suffit de :

<div class="path">Lancer Dolphin, le gestionnaire de fichiers → Cliquer sur la barre de chemin ou appuyer sur Ctrl+L pour l'éditer → Saisir 'smb://[ip-address]'</div><p></p>

{% include screenshot.html image="smb-dolph" %}

Si vous ne connaissez pas l'adresse IP du partage auquel vous souhaitez accéder, vous pouvez aussi *parcourir* le réseau local, en entrant simplement *smb:/* dans la barre d'adresse de Dolphin. Cependant cela ne peut fonctionner que si vous avez au préalable configuré ou désactiver (temporairement) le parefeu. Nous ajouterons bientôt plus d'instructions à ce sujet.

### 13.2.2 Partager vos fichiers

Pour partager *vos* fichiers avec des utilisateurs de MX Windows, Mac OWX ou même d'autres systèmes GNU/Linux via votre réseau local, vous devez configurer le serveur Samba (assurez-vous que les paquets *yast2-samba-server* et *samba* soient installés). Vous n'avez besoin d'effectuer les 3 premières étapes que la première fois que vous voulez partager un dossier.

1) Ouvrir le module YaST Serveur Samba

<div class="path">YaST =&gt; Services réseau  =&gt; Serveur Samba</div><p></p>

{% include screenshot.html image="samba-server" %}

2) Dans l'onglet *Démarrage*, sélectionnez si vous souhaitez que le service Samba démarre automatiquement au démarrage de la machine et s'il faut ouvrir les ports nécessaires dans le parefeu.

3) Dans l'onglet *Partages*, cochez les options *Autoriser les utilisateurs à partager leur répertoire* et *Autoriser l'accès invité*. Dans l'onglet *Identité* vous pouvez configurer votre groupe de travail et le nom du partage.

4) Ajouter des partages en cliquant sur le bouton *Ajouter* puis en spécifiant les répertoires que vous souhaitez partager.

## 13.3 Exécuter des applications MS Windows

Bien que des applications de grande qualité et natives pour GNU/Linux existent pour à peu près tous les usages, il est cependant possible que vous soyez dépendants d'une application disponible sous MS Windows uniquement pour une tâche en particulier. Dans un tel cas, voici les options qui s'offrent à vous :

{% include note.html note="Vous ne devriez Utiliser des applications non natives qu'en dernier recourt. Les applications fonctionnent mieux dans leur environnement d'origine." %}

### 13.3.1 Wine

Wine (Wine Is Not an Emulator: Wine n'est pas un émulateur) est une application qui vous permet d'exécuter certaines applications MS Windows et que vous pouvez installer via YaST ou zypper. Wine est une application en ligne de commande et sa syntaxe est la suivante :

<div class="cl">wine /path/to/setup.exe</div><p></p>

{% include tip.html tip="Le paquet [q4wine](http://sourceforge.net/projects/q4wine/) fournit une interface graphique à certaines fonctionnalités de Wine." %}

Le project Wine maintient une base de données permettant de partager les expériences des utilisateurs et disponible à l'adresse :

[http://appdb.winehq.org/appbrowse.php](http://appdb.winehq.org/appbrowse.php)

### 13.3.2 PlayOnLinux

[PlayOnLinux](http://www.playonlinux.com/) est un logiciel basé sur Wine et disposant d'une d'une interface graphique. Il vous permet d'installer et d'utiliser facilement (certaines) application MS Windows.

### 13.3.2 CrossOver

CrossOver n'est pas gratuit, ni libre. C'est un produit spécialisé dans l'exécution que quelques unes des applications MS Windows les plus courantes, principalement des logiciels bureautiques.

[https://www.codeweavers.com/products/cxlinux/](https://www.codeweavers.com/products/cxlinux/)

### 13.3.3 Dual Boot

Ainsi que nous l'avons mentionné dans le chapitre *Installation*, il est relativement simple d'exécuter GNU/Linux et MS Windows sur le même ordinateur. Si vous n'avez besoin que de quelques applications de temps à autres, cela peut valoir le coup de redémarrer sous MS Windows le temps de les utiliser.

### 13.3.4 Virtualisation

Il est possible d'exécuter MS Windows au sein de GNU/Linux, à l'intérieur d'une *machine virtuelle* en utilisant des logiciels tels que VirtualBox, KVM, Xen ou VMware. Il s'agît là d'un usage avancé qui requiert une certaine puissance de la part de votre ordinateur.
