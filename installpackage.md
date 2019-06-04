---
layout: default
title: 11. Installation de logiciels - Installer les programmes avec le gestionnaire de paquets
permalink: installationpaquets
---

# 11. Installation d'un logiciel

L'installation d'un logiciel est généralement très facile sur openSUSE. Il y a un gestionnaire de paquets, qui vous permet d'installer et de supprimer des paquets très facilement - c'est comparable aux app stores que l'on trouve sur de nombreux smartphones modernes.

## 11.1 Utilisation du gestionnaire de paquets

Ouvrez simplement YaST Software Management.

{% include video.html video="installpackage114" screenshot="sw-single" size="0.99 MB" %}

<center><video width="600" height="450" controls>
	<!-- MP4 must be first for iPad! -->
	<source src="/opensuse-guide-fr/video/installpackage114.mp4" type="video/mp4"  /><!-- Safari / iOS, IE9 -->
	<source src="/opensuse-guide-fr/video/installpackage114.ogv" type="video/ogg"  /><!-- Firefox3.6+ / Opera 10.5+ -->
	<!-- fallback to Flash: -->
</video></center>

Maintenant, recherchez le paquet que vous voulez, sélectionnez-le pour l'installation et cliquez sur Accepter. Le gestionnaire de paquets récupérera alors le paquet RPM à partir de vos dépôts de logiciels configurés - et l'installera, y compris toutes les dépendances. Une fois l'installation terminée, l'application devrait apparaître dans le menu de lancement (sauf s'il s'agit d'un programme en ligne de commande).


{% include tip.html tip="La disponibilité des logiciels dans le gestionnaire de logiciels dépend des _dépôts de logiciels_ configurés. Pour en savoir plus sur les dépôts de logiciels, lisez le chapitre suivant." %}

### 11.1.1 Utilisation de l'installation en 1-clic

Lorsque vous naviguez sur des sites Web liés à openSUSE, il est probable que vous rencontriez des boutons tels que celui-ci :

<center><img class="pic" alt="oneclick" src="{{ site.baseurl | append: '/images/pics/oneclick.png' | replace: '//', '/' }}" /></center>

L'installation en 1 clic (également appelée "Installation directe") automatise simplement le processus d'ajout d'un ou plusieurs dépôts de logiciels au gestionnaire de paquets et l'installation d'un ou plusieurs paquets RPM. Par conséquent, l'installation en 1 clic _devrait être utilisée avec le même soin_ que l'ajout manuel de dépôts non officiels (voir le chapitre suivant pour en savoir plus sur les dépôts de logiciels).

## 11.2 Autres méthodes d'installation

La plupart des utilisateurs trouveront tout ce dont ils ont besoin et plus encore dans le gestionnaire de paquets - surtout si quelques dépôts de logiciels supplémentaires sont ajoutés (voir chapitre suivant). Mais tous les logiciels ne sont pas empaquetés et fournis via des dépôts, et les logiciels non-libres ne peuvent généralement pas être redistribués légalement via le gestionnaire de paquets en raison des restrictions de licence.

Dans ces cas, vous devrez aller sur le site Web du développeur/fournisseur et télécharger et installer le logiciel manuellement - mais **toujours** rechercher d'abord un paquet openSUSE dans les dépôts - et vous assurer que vous téléchargez et installez uniquement des logiciels de **sources fiables**.

### 11.2.1 fichier RPM

Avec un peu de chance, le site web du développeur/vendeur aura un fichier RPM pour openSUSE. Pour installer un seul fichier RPM téléchargé :

<div class="path">Ouvrez le gestionnaire de fichiers Dolphin =&gt; Naviguer vers le fichier RPM =&gt; Cliquez avec le bouton droit de la souris => Ouvrir avec... => Installer/Supprimer des logiciels</div><p></p>

{% include note.html note="N'installez que les fichiers RPM qui sont conçus spécifiquement pour (votre version de) openSUSE." %}

### 11.2.2 Archives Tarball

Si le site Web n'a pas de RPM pour openSUSE, il aura très probablement un fichier archive _tarball_. Les archives Tarballs (\*.tar.gz, \*.tar.bz2) sont simplement des archives compressées similaires aux fichiers ZIP et RAR. Pour décompresser une archive :

<div class="path">Ouvrez le gestionnaire de fichiers Dolphin =&gt; Naviguer vers l'archive =&gt; Cliquez avec le bouton droit de la souris =&gt; Extraire l'archive</div>

L'archive peut contenir des binaires qu'il suffit d'exécuter, ou il peut contenir du code source qui doit être compilé pour fonctionner sur votre système - cela peut être très compliqué, et vous devez d'abord installer divers outils de développement. Il n'y a pas de méthode standard pour installer le contenu de l'archive, mais les instructions doivent toujours être incluses dans l'archive dans des fichiers appelés INSTALL, README ou similaires - ou vous devriez pouvoir trouver les instructions d'installation sur le site Web où vous avez téléchargé l'archive.

## 11.3 Gestion des paquets dans le terminal

Si vous le souhaitez, vous pouvez également installer et supprimer des paquets via un terminal.

Pour rechercher un paquet, utiliser : _zypper search [search term]_. Exemple:

<div class="cl">zypper search thunder</div>

Pour installer un paquet, utiliser :  _zypper install [package name]_. Exemple:

<div class="clroot">zypper install MozillaThunderbird</div>

Pour supprimer un paquet, utiliser : _zypper remove [package name]_. Example:

<div class="clroot">zypper remove PackageKit</div>

Voir _man zypper_ pour plus d'informations.

<div class="cl">man zypper</div>

Ou pour de l'aide sur les commandes individuelles, utilisez par exemple :

<div class="cl">zypper install --help</div>

### 11.3.1 Utilisation de 1-click dans le terminal

Vous pouvez aussi utiliser l'installation en 1 clic dans le terminal, la syntaxe est _OCICLI[URL]_, Exemple :

<div class="clroot">OCICLI http://opensuse-community.org/nvidia.ymp</div>

### 11.3.2 Fichier RPM téléchargé manuellement

Pour installer un fichier RPM téléchargé manuellement, utilisez :

<div class="clroot">zypper install /chemin/vers/lefichier_manuellement_téléchargé.rpm</div>

### 11.3.3 Informations sur les paquets RPM

Vous pouvez obtenir très facilement plusieurs informations utiles sur les paquets installés à partir de la base de données RPM.

Vérifiez quelle version est installée. Exemple :

<div class="cl">rpm -q MozillaFirefox</div>

Listez les fichiers qui sont installés par un paquet, et où ils sont. Exemple :

<div class="cl">rpm -ql amarok</div>

Découvrez à quel paquet appartient un certain fichier. Exemple :

<div class="cl">rpm -qf /usr/bin/firefox</div>

Obtenez diverses informations sur un paquet, y compris le journal des modifications. Exemple :

<div class="cl">rpm -qi --changelog MozillaFirefox</div>
