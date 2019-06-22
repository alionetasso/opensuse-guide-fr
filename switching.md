---
layout: default
title: 2. Changer pour GNU/Linux - Avantages et défis de la migration vers GNU/Linux
permalink: migrer
---

# 2. Migrer vers GNU/Linux

Migrer vers un nouveau système d'exploitation très différent demande des efforts, même si c'est sur le même ordinateur - bien sûr vous n'avez pas à migrer complètement, rien ne vous empêche d'utiliser deux systèmes d'exploitation ou plus. Ce chapitre décrit quelques points à considérer avant de vous aventurer dans le monde merveilleux de GNU/Linux.

## 2.1 Pourquoi utiliser GNU/Linux ?

Il y a de nombreuses raisons pour lesquelles des millions de personnes aiment utiliser GNU/Linux - des raisons de nature technique, financière, éthique ou philosophique, selon le point de vue de chacun.  Voici une liste des raisons les plus courantes pour choisir GNU/Linux :

- **Sécurité :** Il n'y a pratiquement pas de virus pour Linux, ni de *spyware* ou autres menaces.  
- **Maintenance :** Oubliez les soucis liés à l'analyse des fichiers pour détecter les virus, défragmenter le disque, nettoyer le registre, redémarrer l'ordinateur, etc .
- **Stabilité :** GNU/Linux est très stable. Les applications peuvent planter individuellement, mais le système d'exploitation lui-même plante très rarement.
- **Logiciel libre/open source :** Vous pouvez exécuter le logiciel comme vous le souhaitez, étudier le code source, le modifier, le partager. Aucun contrat de licence d'utilisateur final avec clauses en petits caractères ;
- **Standards ouverts:** GNU/Linux et les applications développées pour lui prennent généralement en charge les standards ouverts, permettant une interopérabilité transparente avec d'autres plates-formes et évitant la [dépendance aux fournisseurs](https://fr.wikipedia.org/wiki/Enfermement_propriétaire)
- **Communauté :** GNU/Linux a été décrit comme un "sport d'équipe international" ;
- **Economie :** la plupart des distributions GNU/Linux peuvent être téléchargées gratuitement et il en va de même pour un grand nombre d'applications à leur disposition. De plus, les exigences matérielles relativement modestes vous éviteront de devoir mettre souvent à niveau votre matériel.
- **Légalité :** l'accès à des *logiciels* de haute qualité gratuitement et légalement signifie moins de tentation d'utiliser des copies illégales non autorisées de logiciels propriétaires. Vous ne soutiendrez pas non plus un monopole bien connu pour diverses condamnations pour abus de votre position dominante sur le marché.
- **Transparence :** la plupart des distributions GNU/Linux sont développées dans des espaces ouverts, en utilisant des listes publiques *e-mail*, des canaux IRC publics, des  *bug trackers* publics, des suiveurs de fonctionnalités (*feature trackers*) publics, etc...
- **Diversité :** il existe plusieurs distributions GNU/Linux développées par différentes entreprises ou projets communautaires, pour différents objectifs, offrant différentes expériences utilisateur.
- **Confidentialité :** Les *logiciels* libres respectent généralement votre vie privée, et le code source accessible au public offre une certaine protection contre les *backdoors* et autres activités similaires ;
- **Essayez quelque chose de nouveau** : le simple fait d'essayer quelque chose de nouveau et de différent peut être, en soi, une motivation pour de nombreuses personnes. Et....
- *c'est très amusant !*

{% include pic.html image="hardware.gif" %}

## 2.2 Les défis de la migration

Bien qu'il y ait de nombreux avantages à utiliser GNU/Linux, il peut aussi être difficile de passer à quelque chose de nouveau, de différent et de moins *mainstream* (moins commun):

- **Courbe d'apprentissage :** Vous devrez apprendre à utiliser un nouveau système d'exploitation quelque peu différent, ainsi que de nouvelles applications - et vous devrez *désapprendre* une grande partie de ce que vous avez appris en utilisant d'autres systèmes d'exploitation ;
- **Manque d'applications et de jeux :** Des applications qui vous sont familières, généralement Microsoft Office, Adobe Photoshop, et la plupart des grands jeux populaires peuvent vous manquer. Le *dual-boot*, *WINE* (logiciel permettant de faire fonctionner sur Linux certaines applications prévues pour Windows) et les [machines virtuelles](https://fr.wikipedia.org/wiki/Machine_virtuelle) offrent des solutions partielles à ce problème. Et, bien sûr, il existe des alternatives de haute qualité à GNU/Linux ;
- **Manque de support pour certains matériels :** la plupart des périphériques sont supportés, mais pas tous - avant d'acheter de nouveaux composants matériels, il est recommandé de faire un peu de recherche - plus les composants sont récents et moins répandus, plus le risque de problèmes est grand.  
- **Plus grande difficulté à obtenir de l'aide :** souvent les amis, la famille et les collègues ne seront pas en mesure de vous aider si vous avez des problèmes avec GNU/Linux, donc vous devrez peut-être demander de l'aide *en ligne*, ce qui est souvent moins efficace que de demander de l'aide en direct à quelqu'un que vous connaissez.

## 2.3 Stratégie

Comme la migration n'est pas toujours facile, voici quelques conseils :

- **Soyez réaliste :** Ne vous attendez pas à maîtriser GNU/Linux en une semaine ou deux, comme vous avez maîtrisé le système d'exploitation précédent après peut-être 10 ans d'utilisation ou plus. Et ne vous attendez pas à ce que GNU/Linux soit parfait ;
- **Changez progressivement :** Commencez par installer GNU/Linux sur un ordinateur secondaire, ou dans une configuration *dual-boot* qui conserve votre système d'exploitation précédent à côté du nouveau système, ou encore dans une machine virtuelle. Commencez par apprendre les bases et résolvez les problèmes calmement, un à la fois.
- **Obtenez de l'aide :** N'ayez pas peur de demander de l'aide en ligne ou ailleurs.

### 2.3.1 Applications GNU/Linux sous MS Windows et Mac OSX

Si vous commencez à utiliser les applications disponibles pour GNU/Linux dans votre système d'exploitation actuel, changer plus tard de système sera d'autant plus facile. Voici quelques exemples d'applications gratuites disponibles pour GNU/Linux et MS Windows pour des tâches courantes - la plupart d'entre elles sont également disponibles pour Mac OSX.

<table width="98%">
	<tbody><tr>
		<td class="small-bold"><em>Logiciels</em> libres</td>
		<td class="small-bold"></td>
		<td class="small-bold"><em>Logiciels</em> propriétaires</td>
	</tr>

	<tr>
		<td valign="top">
		<a href="http://www.mozilla.org/firefox/" target="_blank">Firefox</a> (Navigateur web)<br>
		<a href="http://www.mozilla.org/thunderbird/" target="_blank">Thunderbird</a> (Client de courrier électronique)<br>
		<a href="http://www.seamonkey-project.org/" target="_blank">SeaMonkey</a> (Suite d'applications Internet)<br>
		<a href="http://www.pidgin.im/" target="_blank">Pidgin</a> (Messagerie instantanée)<br>
		<a href="http://filezilla-project.org/" target="_blank">FileZilla</a> (Client FTP)<br>
		<a href="http://qbittorrent.sourceforge.net/" target="_blank">qBittorent</a> (Client BitTorrent)<br>
		<a href="http://www.qutecom.org/" target="_blank">QuteCom</a> (VoIP)<br>
		<a href="http://www.linphone.org/" target="_blank">Linphone</a> (VoIP)<br>
		<a href="http://gpodder.org/" target="_blank">gPodder</a> (Gestionnaire de podcast)<br>
		<a href="http://bluegriffon.org/" target="_blank">BlueGriffon</a> (Éditeur HTML)<br>
		<a href="http://gimp-win.sourceforge.net/" target="_blank">GIMP</a> (Édition avancée d'images)<br>
		<a href="http://www.inkscape.org" target="_blank">Inkscape</a> (Graphiques vectoriels)<br>
		<a href="http://hugin.sourceforge.net/" target="_blank">Hugin</a> (Création de panoramas photos)<br>
		<a href="http://www.libreoffice.org/" target="_blank">LibreOffice</a> (Suite bureautique)<br>
		<a href="http://www.scribus.net/" target="_blank">Scribus</a> (Publication assistée par ordinateur)<br>
		<a href="http://gnucash.org/" target="_blank">GnuCash</a> (Comptabilité personnelle/petite entreprise)<br>
		</td>
	<td valign="top">
    <a href="http://www.abisource.com/" target="_blank">Abiword</a> (Traitement de texte simple)<br />
    <a href="http://sourceforge.net/projects/free-cad/" target="_blank">FreeCAD</a> (CAO 3D)<br />
    <a href="http://librecad.org/" target="_blank">LibreCAD</a> (CAO 2D)<br />
    <a href="http://www.blender.org" target="_blank">Blender</a> (Animation 3D)<br />
    <a href="http://calibre-ebook.com/" target="_blank">Calibre</a> (Gestionnaire de bibliothèques numériques)<br />
    <a href="http://www.videolan.org/" target="_blank">VLC</a> (Lecteur multimédia)<br />
    <a href="http://smplayer.sourceforge.net/" target="_blank">SMPlayer</a> (Lecteur multimédia)<br />
    <a href="http://www.clementine-player.org/" target="_blank">Clementine</a> (lecteur audio)<br />
    <a href="http://audacity.sourceforge.net/" target="_blank">Audacity</a> (Éditeur audio)<br />
    <a href="http://lmms.sourceforge.net/" target="_blank">LMMS</a> (Création musicale)<br />
    <a href="http://kid3.sourceforge.net" target="_blank">Kid3</a> (Éditeur de tags audio)<br />
    <a href="http://edu.kde.org/marble/download.php" target="_blank">Marble</a> (Globe virtuel)<br />
    <a href="http://gramps-project.org/" target="_blank">Gramps</a> (Logiciel de généalogie)<br />
    <a href="https://edu.kde.org/kstars/#download" target="_blank">KStars</a> (Planétarium)<br />
    <a href="http://www.stellarium.org/" target="_blank">Stellarium</a> (Planétarium)<br />
	</td>
	<td valign="top">
		<a href="http://opera.com/" target="_blank">Opera</a> (Navigateur Web)<br>
		<a href="https://www.google.com/chrome" target="_blank">Google Chrome</a> (Navigateur Web)<br>
		<a href="http://www.skype.com" target="_blank">Skype</a> (VoIP)<br>
		<a href="http://earth.google.com/" target="_blank">Google Earth</a> (Globe virtuel)<br>
		<a href="http://www.adobe.com" target="_blank">Adobe Reader</a> (Lecteur de PDF)<br>
		<a href="http://www.desura.com/" target="_blank">Desura</a> (Service de distribution de jeux)<br>
		<a href="http://www.3ds.com/products/draftsight/free-cad-software/" target="_blank">Draftsight</a> (CAO)<br>
	</td>
	</tr>
</tbody></table>

Beaucoup d'applications KDE (voir chapitres suivants), sont également disponibles pour MS Windows et Mac OSX - mais elles n'en sont qu'à leurs débuts sur ces plateformes. Pour plus d'informations, consultez :

- [http://windows.kde.org](http://windows.kde.org)
- [http://mac.kde.org](http://mac.kde.org)

Sous Mac OSX, vous pouvez également installer des applications KDE et de nombreux autres logiciels libres via le projet [MacPorts](http://www.macports.org/) ou le projet [Fink](http://www.finkproject.org/).
