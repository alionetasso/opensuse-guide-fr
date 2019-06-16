---
layout: default
title: 4. Installation - Comment installer openSUSE sur son ordinateur
permalink: installation
---

# 4. Installation

Ceci n'est qu'une brève description de l'installation d'openSUSE. Pour une aide plus complète, consultez la documentation officielle.

## 4.1 Avant l'installation

Avant de commencer, vous devez faire attention à certaines choses.

### 4.1.1 Configuration minimale requise

- **CPU :** processeur AMD64 ou Intel64
- **Memoire RAM :** minimum 1GB (2GB recommandé)
- **Disque dur :** 5,0 Go pour une installation normale (plus recommandé). La fonction de snapshots de btrfs a besoin d'au moins 12 Go d'espace disque.
- **Carte son et carte graphique** : La plupart des cartes actuelles sont supportées

### 4.1.2a Graver les ISO sur un DVD

Lorsque vous gravez les fichiers ISO téléchargés sur un DVD, il est important de ne pas oublier de les graver en ISO/images avec votre logiciel de gravure de CD/DVD, sinon le support ne sera pas amorçable.

### 4.1.2b Créer une clé USB

L'ISO peut également être placé sur une clé USB, voir les instructions à ce sujet sur ces pages en fonction des systèmes d'exploitation dont vous disposez :

- openSUSE ou autre Linux: [http://en.opensuse.org/SDB:Live_USB_stick](http://en.opensuse.org/SDB:Live_USB_stick)
- Microsoft Windows: [https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Windows](https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Windows)
- Mac OS X: [https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Mac_OS_x](https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Mac_OS_x)
- La documentation française propose des méthodes pour les trois systèmes : [https://fr.opensuse.org/SDB:Live_USB_stick](https://fr.opensuse.org/SDB:Live_USB_stick)

### 4.1.3 Configurer le BIOS

Si votre ordinateur ne démarre pas à partir du support DVD ou USB, vérifiez que le BIOS de l'ordinateur est configuré pour démarrer à partir de CD/DVD ou USB.

### 4.1.4 Dual boot (openSUSE et MS Windows sur le même ordinateur)

Avoir openSUSE et MS Windows installés sur le même ordinateur est généralement assez simple si MS Windows a été installé en premier. Pendant l'installation, openSUSE détectera MS Windows et le chargeur de démarrage affichera un menu à chaque démarrage vous permettant de choisir si vous voulez démarrer openSUSE ou MS Windows.

openSUSE doit être installé sur une partition/disque séparée. Il est recommandé de libérer de l'espace au préalable à l'aide d'un outil de partitionnement que vous connaissez bien. Mais vous pouvez aussi laisser l'installateur openSUSE redimensionner vos partitions MS Windows - il est fortement recommandé de défragmenter la partition MS Windows avant de le faire.


### 4.1.5 Connecter le câble réseau et activer les périphériques

Si vous branchez votre câble réseau et allumez votre imprimante et les autres périphériques avant de commencer l'installation, il y a de fortes chances qu'ils soient détectés et configurés automatiquement.

## 4.2 Le processus d'installation

Lorsque vous êtes prêt, insérez le DVD ou la clé USB et (re)démarrez l'ordinateur.

### Démarrer l'installation

<table>
	<tr>
		<td width="205" valign="top"><a href="images/installation/dvd/grub.png" rel="thumbnail"><img src="images/installation/dvd/grubb.png" alt="grub" class="pic" /></a></td>
		<td valign="top">Vous obtenez un menu.<br /><br />
		Ici, vous pouvez sélectionner la langue de votre choix en appuyant sur la touche F2 et quelques autres options, puis commencer l'installation.</td>
	</tr>
</table><br />

### Langue, clavier et licence

<table>
	<tr>
		<td width="205" valign="top"><a href="images/installation/dvd/inst-welcome.png" rel="thumbnail"><img src="images/installation/dvd/inst-welcomeb.png" alt="welcome" class="pic" /></a></td>
		<td valign="top">Le contrat de licence ne vise qu'à vous informer de vos droits. Il n'exige pas votre acceptation, puisqu'il ne limite pas votre utilisation.<br /><br />
		Vérifiez que la langue et la disposition du clavier sont conformes à vos souhaits.</td>
	</tr>
</table><br />

### Interface utilisateur

<table>
	<tr>
		<td width="205" valign="top"><a href="images/installation/dvd/inst-desktop.png" rel="thumbnail"><img src="images/installation/dvd/inst-desktopb.png" alt="inst-desktop" class="pic" /></a></td>
		<td valign="top">Différentes interfaces graphiques (environnements de bureau) existent pour GNU/Linux. L'espace de travail Plasma de KDE est présélectionné et est préféré par environ 70% des utilisateurs d'openSUSE et est également l'objet de ce guide. Mais vous pouvez aussi choisir le bureau GNOME ou l'installation d'un serveur en mode texte.<br /><br />
		Sous "Personnalisé", vous pouvez sélectionner manuellement différents motifs, y compris les environnements de bureau légers comme Xfce.</td>
	</tr>
</table><br />

### Partitionnement

<table>
	<tr>
	  <td width="205" valign="top"><a href="images/installation/dvd/inst-disk.png" rel="thumbnail"><img src="images/installation/dvd/inst-diskb.png" alt="inst-disk" class="pic" /></a></td>
	  <td valign="top">Par défaut openSUSE proposera de créer trois nouvelles partitions / (root) pour les fichiers système, /home/ pour les fichiers personnels des utilisateurs et swap qui est utilisé comme un complément pour la RAM, similaire au fichier d'échange pagefile.sys dans MS Windows.<br /><br />
	  Vérifiez toujours que la proposition de partitionnement est ce que vous voulez, et si vous effectuez une installation en dual boot, faites très attention, pour vous assurer que tout est comme vous le souhaitez.<br /><br />
	  Notez que Linux étiquette les disques/partitions en utilisant le schéma suivant - <i>sda1</i> est la première partition sur le premier disque, <i>sdb3</i> est la troisième partition sur le deuxième disque, et ainsi de suite. Les partitions qui seront formatées sont écrites en rouge.</td>
	</tr>
</table><br />

### Horloge et fuseau horaire

<table>
	<tr>
		<td width="205" valign="top"><a href="images/installation/dvd/inst-time.png" rel="thumbnail"><img src="images/installation/dvd/inst-timeb.png" alt="inst-time" class="pic" /></a></td>
		<td valign="top">Sélectionnez le fuseau horaire ici.<br /><br />Si vous n'avez que GNU/Linux, il est recommandé de régler l'horloge matérielle sur UTC, si vous avez un dual-boot avec MS Windows, réglez-la à l'heure locale..</td>
	</tr>
</table><br />


### Créer un nouvel utilisateur

<table>
	<tr>
	<td width="205" valign="top"><a href="images/installation/dvd/inst-user.png" rel="thumbnail"><img src="images/installation/dvd/inst-userb.png" alt="inst-user" class="pic" /></a></td>
	<td valign="top">Il est maintenant temps de créer votre utilisateur. Notez que par défaut, le mot de passe de l'utilisateur root (administrateur) sera le même que celui de l'utilisateur normal.<br /><br />
	Si vous voulez avoir la sécurité supplémentaire d'un mot de passe root séparé, pensez à décocher cette case. Vous pouvez également envisager de désactiver l'autologin pour empêcher les gens d'accéder facilement à votre système et à vos données.</td>
	</tr>
</table><br />

### Paramètres d'installation

<table>
	<tr>
		<td width="205" valign="top"><a href="images/installation/dvd/inst-overview.png" rel="thumbnail"><img src="images/installation/dvd/inst-overviewb.png" alt="inst-overview" class="pic" /></a></td>
		<td valign="top">Vérifiez deux fois que tout est comme vous le souhaitez - c'est le point de non-retour !</td>
	</tr>
</table><br />

### Installation proprement dite

<table>
	<tr>
		<td width="205" valign="top"><a href="images/installation/dvd/inst-inst.png" rel="thumbnail"><img src="images/installation/dvd/inst-instb.png" alt="inst-inst" class="pic" /></a></td>
		<td valign="top">L'installation est alors effectuée. Une fois terminé, le système redémarre et est prêt à être utilisé.<br /><br />
Amusez-vous bien avec openSUSE !</td>
	</tr>
</table><br />
