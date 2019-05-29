---
layout: default
title: 8. Sécurité et root - sécurité de base et travailler en tant qu'utilisateur root
permalink: securite
---

# 8. Sécurité et root

openSUSE et GNU/Linux en général est un système d'exploitation très sécurisé, mais lorsque vous utilisez n'importe quel ordinateur sur Internet, vous devez toujours être prudent.

## 8.1 L'utilisateur root

L'une des raisons pour lesquelles GNU/Linux est très sûr, c'est que vous ne travaillez normalement pas avec les permissions administrateur - seul l'utilisateur *root* (ou *super utilisateur*) a les permissions administratives complètes.

Le mot de passe *root* vous sera demandé lors de l'installation de paquets ou d'autres tâches administratives en dehors de votre répertoire /home/. A moins que vous n'ayez décoché la case pendant l'installation, l'utilisateur *root* a le même mot de passe que votre utilisateur normal.

{% include note.html note="Ne travaillez en tant que *root* que lorsque c'est nécessaire." %}

### 8.1.1 Gestionnaire de fichiers super utilisateur

Pour travailler graphiquement avec les fichiers système qui nécessitent des permissions *root*, vous pouvez lancer le gestionnaire de fichiers Dolphin en mode *super utilisateur*.

{% include screenshot.html image="super-dolph" %}

### 8.1.2 Travailler en tant qu'utilisateur root dans le terminal

La commande suivante est utilisée pour passer à l'utilisateur *root* dans un terminal :

<div class="cl">su -</div><p></p>

{% include tip.html tip="Rien n'apparaîtra à l'écran pendant que vous tapez votre mot de passe. C'est le but recherché." %}

Pour arrêter de travailler en tant que root, entrez la commande suivante :

<div class="clroot">exit</div>

Pour exécuter une seule commande en tant que root, vous pouvez utiliser :

<div class="cl">su -c "[command]"</div>

Pour en savoir plus sur l'utilisation du terminal, reportez-vous au chapitre suivant.

## 8.2 Mises à jour de sécurité

Lorsque de nouvelles mises à jour sont disponibles, vous serez averti par l'applet de mise à jour qui s'exécute dans la zone de la barre d'état système :

{% include screenshot.html image="pk-updater" %}

La mise à jour peut se faire graphiquement en cliquant sur l'applet de mise à jour dans la barre d'état.

### 8.2.1 Installation des mises à jour dans le terminal

Pour installer les correctifs de sécurité officiels et les correctifs de bogues uniquement, exécutez :

<div class="clroot">zypper patch</div>

Pour installer les correctifs officiels ainsi que les mises à jour des dépôts tiers, exécutez :

<div class="clroot">zypper update</div>

## 8.3 Pare-feu

openSUSE est livré avec un pare-feu inclus dans l'installation par défaut ('firewalld'). Par défaut, il autorise tout le trafic sortant et bloque tout le trafic entrant, donc vous n'aurez besoin de changer la configuration que si vous voulez exécuter certains serveurs réseau. Le pare-feu est configurable dans YaST, lisez à propos de YaST dans un chapitre ultérieur.

## 8.4 Vírus et spyware

Il n'est pas nécessaire d'exécuter un antivirus ou de rechercher des logiciels espions. La propagation de logiciels malveillants via Internet et infectant les systèmes de bureau des utilisateurs à domicile normaux est pratiquement inexistante pour GNU/Linux. Assurez-vous simplement que vous n'installez et n'exécutez pas vous-même des logiciels ou des scripts provenant de sources non fiables, et vous serez en sécurité.
