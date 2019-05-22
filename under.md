---
layout: default
title: "Annexe C: Dans les coulisses - À la découverte de ce qu'il se passe sous la surface"
permalink: under
---

# Appendix C: Sous la surface

L'objectif de ce chapitre est de donner au lecteur un aperçu et quelques idées de ce qu'il se passe dans les rouages d'un système d'exploitation openSUSE GNU/Linux.

## C.1 Composants principaux du système

N'importe quel système d'exploitation moderne est un immense et complexe engin, et les distributions GNU/Linux ne font pas exception. Le noyau Linux n'est qu'un composant parmi bien d'autres. L'illustration ci-dessous présente les composants essentiels et leur rôle.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
        <tbody>
        <tr>
        <td style="width: 50%;"><center><a href="{{ site.baseurl | append: '/images/pics/distro.png' | replace: '//', '/' }}" rel="thumbnail"><img src="{{ site.baseurl | append: '/images/pics/distrob.png' | replace: '//', '/' }}" alt="distro" class="pic" /></a></center><br /></td>
        </tr>
        <tr>
        <td class="image-caption">Cette illustration présente les principaux composants d'un système GNU/Linux</td>
        </tr>
        </tbody>
</table>

## C.2 Arborescence

La plupart des utilisateurs n'auront probablement jamais besoin de travailler en dehors de leur dossier *home*. Il n'est toutefois par inutile d'avoir une petite idée du fonctionnement de la hiérarchie des fichiers.

Chez GNU/Linux, il n'y a *qu'une seule* arborescence, contrairement à Microsoft Windows, par exemple, qui dispose d'arborescences différentes pour chacun des systèmes de fichiers et partitions, sous GNU/Linux les systèmes de fichiers ou partitions séparés sont *montés* dans des dossiers au sein d'une seule et même arborescence. Le dossier racine de l'arborescence est "**/**" et les chemins sont écrits à la suite en utilisant d'autre barres obliques (*slashes*).

En conséquence, un chemin ressemblera à cela sous GNU/Linux :

**/home/*utilisateur*/Bureau/**

Chez MS Windows, ce même chemin ressemblerait à cela :

**C:\\Documents and Settings\\*utilisateur*\\Desktop**

{% include tip.html tip="Sous GNU/Linux les noms de fichiers et de dossiers sont **sensibles à la casse (majuscule/minuscule)**." %}

Les utilisateurs normaux ne disposent de permissions en écriture qu'à l'intérieur de leur dossier **/home/** et n'ont que très rarement le besoin de travailler en dehors de ce dernier.

## C.3 Fichiers cachés

Les fichiers et dossiers dont le nom commence par '.' (un point) sont cachés. Sous Dolphin, vous pouvez les afficher via le raccourci clavier **Alt+.** ou via le menu **Affichage → Afficher les fichiers masqués** dans la barre de menu. Sous Nautilus, le gestionnaire de fichiers de GNOME, vous pouvez les afficher via le raccourci clavier **Ctrl+h** ou via le menu dit *hamburger*, en haut à droite puis en cochant **Afficher les fichiers masqués**.

Les applications enregistrent les paramètres des utilisateurs et certaines données qu'elles utilisent dans le dossier *home* des utilisateurs, par exemple sous **/home/*utilisateur*/.mozilla/** ou **/home/*utilisateur*/.config/vlc/** etc. Si vous désinstallez ou réinstallez une application, ses paramètres et données resteront dans le dossier *home*. Pour réinitialiser une application, il vous suffit de renommer, déplacer ou supprimer ces paramètres et données, masqués dans votre dossier *home*.

## C.4 Fichiers de configuration importants

Dans un système GNU/Linux, les configurations et paramètres sont généralement stockés sous la forme de fichier textes, dans un format lisible par l'humain. La plupart des configurations peuvent être faites graphiquement via YaST ou divers autres applications graphiques. Toutefois, il est bon de connaître l'emplacement des fichiers les plus importants.

Les configurations s'appliquant au système entier sont placées dans **/etc/** tandis que les paramètres des utilisateurs sont stockés dans des fichiers cachés dans leurs dossiers *home* respectifs.

<table class="table">
<tbody>
    <tr>
    <td style="width: 230px;"><b>/etc/fstab</b></td>
    <td>La table des systèmes de fichiers, liste les systèmes de fichiers et partitions montés au démarrage.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/sysconfig/yast2</b></td>
    <td>Configuration pour YaST.</td>
    </tr>
    <tr>
    <td style="width: 230px;"><b>/etc/zypp/zypp.conf</b></td>
    <td>Configuration de la gestion des logiciels.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/samba/smb.conf</b></td>
    <td>Configuration de Samba (« Windows Network »)</td>
    </tr>
    <tr>
    <td style="width: 230px;"><b>/etc/HOSTNAME</b></td>
    <td>Le nom de la machine.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/X11/xorg.conf.d/</b></td>
    <td>Fichiers de configuration du serveur X. Par défaut, l'auto détection est utilisée, n'éditez ces fichiers que si vous devez configurer X.</td>
    </tr>
    <tr>
    <td style="width: 230px;"><b>/etc/sysconfig/kernel</b></td>
    <td>Le noyau. Peut servir à charger des modules complèmentaires au démarrage.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/modprobe.d/50-blacklist.conf</b></td>
    <td>Mettre des modules du noyau sur liste noire (interdire leur chargement).</td>
    </tr>
</tbody>
</table>


## C.5 Journaux

En cas de problème, il est utile de connaître l'emplacement des fichiers de *logs* (journaux) principaux, la majorité d'entre eux étant placés dans **/var/log**.

<table class="table">
<tbody>
  <tr>
      <td style="width: 230px;"><b>/var/log/Xorg.0.log</b></td>
      <td>Log du serveur X.</td>
  </tr>
  <tr class="d1">
      <td style="width: 230px;"><b>/home/<i>utilisateur</i>/.xsession-errors</b></td>
      <td>Utile pour débogguer les applications exécutées en tant qu'utilisateur normal.</td>
  </tr>
  <tr class="d1">
      <td style="width: 230px;"><b>/var/log/YaST2/</b></td>
      <td>Journaux des modules et composants YaST.</td>
  </tr>
  </tbody>
</table>

Le journal principal du système peut être visualisé grâce au module YaST *systemd-journal* ou via la commande *journalctl* :

<div class="clroot">journalctl</div>

Il est recommandé de se documenter sur journalctl pour l'utiliser le plus efficacement possible.

## C.6 Déboggage

Voici quelques astuces basiques de déboggage pour GNu/Linux dans le cas où une application dysfonctionne ou ne démarre pas du tout.

- Si une application échoue, essayez de la lancer depuis un terminal afin d'obtenir plus de messages d'information
- Essayez de supprimer ou renommer les dossiers cachés de l'application dans le dossier *home* de l'utilisateur
- Essayez de créer un nouvel utilisateur pour voir si le problème persiste. Si ce n'est pas le cas, la cause se trouve probablement dans les paramètres ou données de l'application présents dans le dossier *home* de l'utilisateur rencontrant le problème
- Vérifiez les fichiers de journaux (*logs*) appropriés

{% include tip.html tip="Réinstaller le logiciel ne résoud généralement rien dans la mesure où les anciens paramètres et/ou données sont conservés dans les dossiers cachés, au sein du dossier *home*." %}
