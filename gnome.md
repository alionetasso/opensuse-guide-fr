---
layout: default
title: 6. Environnement de bureau GNOME - Utilisation et configuration de GNOME sur ordinateur de bureau ou netbook
permalink: gnome
---

# 6. Environnement de bureau GNOME

Si vous avez fait le choix du bureau GNOME lors de l'installation, vous vous retrouverez, au redémarrage après celle-ci, devant GDM, le gestionnaire de connexion de l'environnement GNOME. Une fois connecté, vous vous retrouverez devant un espace simple et épuré, comprenant le bureau lui-même et la barre supérieure.
Celle-ci vous se compose:
- du menu Activités, tout à fait à gauche, qui vous donne accès à vos applications ainsi qu'à une vue générale des fenêtres ouvertes et des espaces de travail ;
- du centre de notification, au centre : c'est là que vous retrouverez les messages du système et des logiciels (alertes, rappels de calendriers, etc..) ainsi que le calendrier ;
- du menu utilisateur, tout à fait à droite, qui vous permet de gérer le son, la luminosité de l'écran, les connexions réseaux et Bluetooth mais aussi d'accéder à votre compte, aux paramètres du système et d'éteindre la machine.

À l'inverse d'un environnement comme KDE Plasma qui est extrêmement personnalisable, GNOME vise à offrir un espace de travail simple, clair, sans fioritures et qui vous permet de vous consacrer à votre tâche. Il peut toutefois être complété grâce à l'ajout d'extensions (voir ci-dessous).

## 6.1 L'environnement de bureau

Ce bureau vise à offrir à ses utilisateurs une nouvelle métaphore d'environnement de bureau et change donc beaucoup par rapport aux environnements plus traditionnels (souvent composés d'une barre des tâches et d'un menu verticial en bas à gauche).
Certaines choses diffèrent donc considérablement de la plupart des autres environnements de bureau :

- la barre des tâches se trouve en haut et affiche plusieurs sous-menus énumérés ci-dessus ainsi que le menu de l'application **au premier plan** ;
- le bureau lui-même n'est qu'un espace destiné à accueillir les fenêtres, il ne sert à afficher les icônes des applications ou des raccourcis vers vos fichiers ;
- la plupart des raccourcis font appel à la touche Super (injustement représentée par le logo Windows sur la plupart des PC), préssée seule cette touche vous donne accès au *Shell* : c'est là que vous allez retrouver l'ensemble de vos applications ainsi qu'une vue étalée de toutes vos fenêtres ouvertes.

<center><a href="images/screenshots/gnome-desktop.png" rel="thumbnail"><img src="images/screenshots/gnome-desktop.png" alt="GNOME Desktop" class="pic" /></a></center><br />

### 6.1.1 Le menu lanceur d'applications

Le menu de lancement s'ouvre en cliquant sur l'icône dans le coin inférieur gauche de l'écran ou en appuyant sur la touche Super ou Alt+F1. Si vous commencez à taper, un champ de recherche apparaîtra en haut. Vous pouvez ajouter et supprimer des applications à vos favoris en cliquant avec le bouton droit de la souris sur les éléments du menu. Vous pouvez ajouter et supprimer des applications à vos favoris en cliquant avec le bouton droit de la souris sur les éléments du menu.

<center><a href="images/screenshots/launchmenu.png" rel="thumbnail"><img src="images/screenshots/launchmenub.png" alt="launchmenuç" class="pic" /></a></center><br />

Vous pouvez modifier des entrées de menu ou en ajouter de nouvelles comme ceci :

<div class="path">Cliquez avec le bouton droit de la souris sur l'icône du menu  =&gt; Modifier les applications...</div>

Pour ajouter un raccourci pour une application sur le bureau ou dans le panneau, vous pouvez le faire (les widgets doivent être déverrouillés) ainsi :

<div class="path">Trouver l'application dans le menu => Clic droit sur l'entrée => Cliquez sur "Ajouter au panneau" ou "Ajouter au bureau"</div>

### 6.1.2 Espace de travail virtuel

Pour éviter que votre bureau ne soit encombré de fenêtres, vous pouvez utiliser des espaces de travail virtuels pour organiser vos applications et être plus productif. Dans le panneau vous trouverez une petite grille, c'est le pager de bureau, utilisez-le pour basculer entre vos bureaux virtuels.

<center><img src="images/screenshots/pager.png" alt="pager" class="pic" /></center><br />

Vous pouvez également utiliser l'effet de grille du bureau pour obtenir une vue d'ensemble de vos bureaux virtuels en plein écran, essayez d'appuyer sur *Ctrl + F8* (nécessite la prise en charge de des effets de bureau, voir le paragraphe sur ce sujet ci-dessous).

## 6.2 Gestion des fichiers

Le gestionnaire de fichiers par défaut est Dolphin, qui est l'un des favoris dans le menu de lancement ou dans la catégorie "Système". Il devrait être très intuitif. Les clés USB et autres supports amovibles apparaîtront automatiquement dans le volet gauche de Dolphin.
<div class="path">Launch Menu => System => Dolphin</div><br />

Vous pouvez également trouver Dolphin comme l'un des favoris dans le menu de lancement des applications.

<center><a href="images/screenshots/dolphin.png" rel="thumbnail"><img src="images/screenshots/dolphinb.png" alt="dolphin" class="pic" /></a></center><br />

## 6.3 Configurer le bureau (Paramètres système KDE)

Les paramètres globaux de KDE sont regroupés de manière pratique en un seul endroit. Ici, vous pouvez configurer presque tout ce qui concerne l'espace de travail de KDE Plasma, y compris le comportement de la souris, les applications par défaut, les associations de fichiers, etc.

<div class="path">Menu lanceur des applications => Applications => Configuration => Configuration du système</div>

Vous pouvez également trouver Configurer le bureau (paramètres système) comme l'un des favoris dans le menu de lancement des applications.

<center><a href="images/screenshots/systemsettings.png" rel="thumbnail"><img src="images/screenshots/systemsettingsb.png" alt="systemsettings" class="pic" /></a></center><br />

<div class="tip">
<table>
<tbody>
<tr>
<td><img src="images/pics/tip.png" alt="tip" /></td>
<td>Ne confondez pas le centre de contrôle KDE utilisé pour la configuration personnelle de l'espace de travail KDE et des applications KDE avec le centre de contrôle YaST utilisé pour les paramètres d'administration à un niveau plus profond du système (Voir plus loin le chapitre sur YaST).</td>
</tr>
</tbody>
</table>
</div><br />

## 6.4 Moniteur système / Tableau des processus

Naturellement, KDE dispose également d'un outil pour surveiller les processus en cours d'exécution et l'utilisation des ressources du système. Appuyez simplement sur *Ctrl+Esc* pour afficher la fenêtre d'activité système.

<center><a href="images/screenshots/systemactivity.png" rel="thumbnail"><img src="images/screenshots/systemactivityb.png" alt="systemactivity" class="pic" /></a></center><br />

Pour un moniteur système avancé et personnalisable, y incluant les graphiques réseau, etc. exécutez le programme *ksysguard*.

## 6.5 Widgets

Le Bureau Plasma de KDE est centré autour de widgets et de conteneurs. Le bureau et le panneau sont des conteneurs dans lesquels des widgets peuvent être placés. Le menu, la barre d'état système, etc. sont simplement des widgets. Beaucoup d'autres widgets sont disponibles.  
Pour ajouter des widgets :

<div class="path">Clic droit sur le bureau => Ajouter des widgets => Glisser des widgets sur le bureau ou le panneau</div>

Pour configurer, déplacer, redimensionner des widgets, etc., cliquez pour ouvrir la boîte à outils dans le coin supérieur droit du bureau. Cela nécessite le déverrouillage des widgets.

<div class="path">Clic droit sur le bureau => Soit "Verrouiller les widgets", soit "Déverrouiller les widgets".</div><br/>

<center><a href="images/screenshots/widgets.png" rel="thumbnail"><img src="images/screenshots/widgetsb.png" alt="widgets" class="pic" /></a></center><br /><br />

## 6.6 Effets de bureau

Le gestionnaire de fenêtres de KDE prend en charge les effets de bureau 3D. Une sélection basique et discrète d'effets est activée par défaut si vous disposez du support matériel et des pilotes appropriés en place. Essayez d'appuyer sur *Ctrl+F8* ou *Ctrl+F9* par exemple.

Vous pouvez désactiver ou activer d'autres/plusieurs effets dans Paramètres système.

<center><a href="images/screenshots/effects.png" rel="thumbnail"><img src="images/screenshots/effectsb.png" alt="effects" class="pic" /></a></center><br />

Le raccourci clavier pour activer/désactiver temporairement les effets de bureau est *Alt+Maj+F12*.
