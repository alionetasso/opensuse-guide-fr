---
layout: default
title: 12. Dépôts de logiciels - Ajout et gestion des dépôts de paquets
permalink: depots
---

# 12. Dépôts de logiciels

Comme mentionné dans le chapitre précédent, le gestionnaire de paquets installe un logiciel en récupérant le paquet et ses dépendances dans les dépôts de logiciels, donc les logiciels disponibles pour une installation facile via le gestionnaire de paquets dépendent des dépôts configurés.

Un dépôt logiciel est une collection de paquets RPM (le format d'empaquetage d'openSUSE) et de métadonnées pour les paquets disponibles. Habituellement, les dépôts se trouvent sur des serveurs en ligne, mais ils peuvent aussi se trouver sur un CD/DVD ou sur d'autres supports.

## 12.1 Gestion des dépôts

Les dépôts de logiciels peuvent être ajoutés, supprimés et configurés via YaST, dans le module Dépôts de logiciels.

{% include screenshot.html image="yast-repos" %}

### 12.1.1 Ajout de dépôts

Les dépôts officiels sont préconfigurés, mais de nombreux dépôts non officiels existent et peuvent être ajoutés.

{% capture repositories_obs %}
Ajoutez les dépôts avec prudence.

- Les dépôts non officiels peuvent inclure des paquets expérimentaux
- Tous les dépôts ne sont pas compatibles entre eux
- Le niveau de risque d'un dépôt peut changer avec le temps
- Trop de dépôts ralentit le gestionnaire de paquets
{% endcapture %}
{% include note.html note=repositories_obs %}

La façon la plus simple et la plus sûre d'ajouter des dépôts est d'utiliser la liste des dépôts communautaires en ligne de YaST. Vous disposez ainsi d'une sélection de dépôts populaires et assez sûrs :

<div class="path">YaST => Logiciels => Dépôts de logiciels => Cliquez sur "Ajouter" => Selectionner "Dépôts communautaires" et cliquez sur "Suivant"</div><p></p>

<center><video width="600" height="450" controls="controls">
  <source src="/video/repos114.mp4" type="video/mp4" />
  <source src="/video/repos114.ogv" type="video/ogg" />
  Vous n'avez pas de navigateur moderne, donc pas de balise video HTML5 ! Essayez Firefox.
</video></center>

Notez que *openSUSE BuildService* est un service permettant à la communauté de créer et de partager des paquets. *Les dépôts openSUSE BuildService ne sont pas officiels et ne sont pas pris en charge*. L'utilisation se fait à **vos propres risques**.

### 12.1.2 Dépôts recommandés

Vous devriez toujours avoir les quatre dépôts *officiels* (qui sont configurés prêts à l'emploi) :<br/>

- **Main Repository (OSS)**
- **Main Repository (NON-OSS)**
- **Main Update Repository**
- **Main Update Repository (NON-OSS)**

De plus, je recommande d'ajouter les dépôts *non-officiels* suivants de la liste des dépôts communautaires, pour avoir un bon équilibre entre la disponibilité et la stabilité des logiciels pour la plupart des utilisateurs.

- **Dépôt Packman**

{% capture repositories_tip %}
Il manque toujours un paquet ?

Vous pouvez rechercher des paquets/dépôts sur openSUSE BuildService ici :

[http://software.opensuse.org/search](http://software.opensuse.org/search)

Ce moteur de recherche de paquets inclut également le dépôt Packman :

[http://webpinstant.com](http://webpinstant.com)

N'oubliez pas d'ajouter des dépôts non officiels avec prudence !
{% endcapture %}
{% include tip.html tip=repositories_tip %}

### 12.1.3 Mises à jour des changements de fournisseur

Mettre à jour les paquets installés d'un dépôt vers des versions d'un autre dépôt avec un autre *fournisseur*, est un peu compliqué. Pour en savoir plus, cliquez ici :

[https://fr.opensuse.org/SDB:Mise_à_jour_avec_changement_de_fournisseur](https://fr.opensuse.org/SDB:Mise_à_jour_avec_changement_de_fournisseur)

## 12.2 Gestion des dépôts dans le terminal

Si vous le souhaitez, vous pouvez également gérer vos dépôts via un terminal.

Ajout d'un dépôt avec auto-refresh activé `zypper addrepo -f[URL][Alias]`. Exemple :

<div class="clroot">zypper addrepo -f http://packman.inode.at/suse/openSUSE_Leap_15.2/ packman</div>

Désactiver un dépôt `zypper modifyrepo -d [URL|Alias]`. Exemple:

<div class="clroot">zypper modifyrepo -d Packman</div>

Supprimer un dépôt `zypper removerepo [URL|Alias]`. Exemple:

<div class="clroot">zypper removerepo http://packman.inode.at/suse/openSUSE_Leap_15.2/</div>

Lister les dépôts configurés, en affichant les détails (priorités, URL, etc.):

<div class="cl">zypper repos -d</div>

Voir `man zypper` pour plus d'informations.

<div class="cl">man zypper</div>

Ou pour de l'aide sur les commandes individuelles, utilisez par exemple :

<div class="cl">zypper addrepo --help</div>
