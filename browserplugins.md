---
layout: default
title: 14. Plugins de navigateur - Installez des plugins pour votre navigateur Web tels que Flash et Java
permalink: browserplugins
---

# 14. Plugins de navigateur

De nombreux sites Web nécessitent l'installation de divers plugins de navigateur pour fonctionner comme il faut. Voici quelques plugins que vous voudrez peut-être installer. N'installez ces plugins que si vous en avez besoin, car ils peuvent avoir un impact sur les performances et la sécurité lorsque vous naviguez sur Internet.

{% include tip.html tip="Si les concepts de *gestionnaire de paquets* et de *dépôts* vous sont étrangers, revisitez les chapitres [Installation de logiciels](installationpaquets) et [Dépôts de logiciels](depots)." %}

## 14.1 Adobe Flash

Installez le package **freshplayerplugin**, si vous avez besoin du support Flash pour certaines vidéos, jeux et autres choses en ligne (*Packman Repository* est requis).

Installation de Flash dans le terminal :

<div class="clroot">zypper addrepo -f http://packman.inode.at/suse/openSUSE_Leap_15.0/ packman</div>

<div class="clroot">zypper install freshplayerplugin</div>

## 14.2 Java

Les applets Web Java sont utilisés pour les jeux, la banque à domicile dans certains pays, et diverses autres choses.

Installez le paquet **java-1_8_8_0-openjdk-plugin** avec le gestionnaire de paquets s'il n'est pas déjà installé.

Installation du plugin de navigateur Java dans le terminal :

<div class="clroot">zypper install java-1_8_0-openjdk-plugin</div>

## 14.3 Streaming vidéo et audio

Pour obtenir la prise en charge de divers flux multimédia dans Firefox et d'autres navigateurs, installez le paquet **xine-browser-plugin** (*Dépôt Packman requis*).

Installation du plugin multimédia dans le terminal :

<div class="clroot">zypper install xine-browser-plugin</div>

## 14.4 Microsoft Silverlight

Microsoft a créé quelque chose appelé Silverlight pour concurrencer Adobe Flash en faisant en sorte que le Web nécessite des extensions propriétaires.

Comme on pouvait s'y attendre Microsoft ne fournit *pas* de plugin officiel pour GNU/Linux, mais il y a quelque chose nommé [Pipelight](http://fds-team.de/cms/articles/2013-08/pipelight-using-silverlight-in-linux-browsers.html) qui apporte Microsoft Silverlight sur GNU/Linux. Vous pouvez trouver le paquet Pipelight pour openSUSE [ici](http://software.opensuse.org/package/pipelight).

Netflix est compatible avec le dernier navigateur Google Chrome Browser, sans avoir besoin de Microsoft Silverlight.

## 14.5 Google Hangouts

Google fournit des services de chat vocal et vidéo sur GNU/Linux via le site de Google à l'aide d'un plugin de navigateur. Téléchargez les fichiers RPM pour openSUSE ici :

[http://www.google.com/chat/video](http://www.google.com/chat/video)
