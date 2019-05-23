---
layout: default
title: "Appendix D: Histoire et contexte - Qu'est-ce que le Logiciel Libre et Open Source et Quelle est l'histoire d'openSUSE ?"
permalink: histoire
---

# Appendix D: Histoire et contexte

Le but de ce chapitre est de donner aux lecteurs un aperçu et une connaissance basique de l'histoire et de l'écosystème de GNU/Linux et des logiciels libres/open source en général..

## D.1 Code source vs Code machine binaire

Les logiciels informatiques sont écrits dans différents langages de programmation. Ce *code source* peut être écrit et compris par toute personne ayant la formation appropriée :

    #include <iostream.h>

    main()
    {
        cout << "Hello World!";
        return 0;
    }

Le code source lisible par l'homme est ensuite compilé en *code machine binaire* que les ordinateurs peuvent exécuter :

    01001000 01100101 01101100 01101100 01101111 00100000 01010111 01101111 01110010 01101100 01100100 00100001 00100000

Sans accès au code source et sans autorisation de le modifier, ni vous en tant qu'individu, ni votre communauté en général, ne pouvez étudier comment le logiciel fonctionne et ce qu'il fait - et encore moins le modifier et l'améliorer - vous êtes totalement dépendant des caprices de la société/personne qui possède le code source.

## D.2 Richard Stallman, GNU et le logiciel libre

En 1984 et 1985 respectivement, le programmeur système Richard M. Stallman (RMS), de plus en plus frustré par les restrictions techniques et sociales imposées par les logiciels propriétaires, créa le projet [GNU](http://www.gnu.org/) (GNU's Not Unix) afin de créer un système d'exploitation libre semblable à Unix et la [Free Software Foundation (FSF)](http://www.fsf.org) une fondation visant à promouvoir les logiciels libres.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
		<td style="width: 50%;"><div style="text-align: center;"><img style="width: 200px; height: 220px;" alt="rms" src="{{ site.baseurl | append: '/images/pics/rms.jpg' | replace: '//', '/' }}" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">Richard M. Stallman</td>
	</tr>
</tbody>
</table>

Logiciel libre ne signifie pas gratuit, le logiciel libre peut être commercial. Libre se réfère à la liberté, spécifiquement définie par les quatre libertés fondamentales suivantes :

- (0) La liberté d'exécuter le programme, pour n'importe quel but.
- (1) La liberté d'étudier le fonctionnement du programme et de le modifier pour qu'il fasse ce que vous voulez.
- (2) La liberté de redistribuer des copies pour que vous puissiez aider votre voisin.
- (3) La liberté d'améliorer le programme, et de diffuser vos améliorations (et les versions modifiées en général) au public, afin que toute la communauté en bénéficie.

Les libertés 1 et 3 nécessitent l'accès au code source du programme.

{% include tip.html tip="Si vous voulez en savoir plus sur les logiciels libres, pensez à télécharger cette [vidéo de Richard M. Stallman en parlant].(http://audio-video.gnu.org/video/20090122_richard_stallman.ogv) (550 MB, Ogg Theora format)" %}

### D.2.1 GNU GPL, Copyleft et autres licences de logiciels libres

Toute licence de logiciel qui garantit les quatre libertés fondamentales mentionnées ci-dessus est considérée comme une licence de logiciel libre. Il existe des dizaines et des dizaines de licences de logiciels libres différentes. Les licences de logiciels libres s'appuient sur les lois existantes sur le droit d'auteur pour offrir aux utilisateurs beaucoup plus de liberté et de droits que ce que vous auriez normalement.

La licence de logiciel libre de loin la plus utilisée est la GNU General Public License (GPL). L'une des caractéristiques de la GNU GPL est qu'elle applique un principe connu sous le nom de *copyleft*. Cela signifie que même si vous êtes autorisé à modifier et redistribuer des logiciels sous GPL - ces travaux dérivés **doivent** être distribués sous des conditions similaires - assurant ainsi que les programmes sous GPL resteront toujours des logiciels libres. Les licences sans copyleft sont aussi appelées licences *permissives*, ces types de licences de logiciels libres permettent de redistribuer le logiciel sous différentes licences incompatibles, même propriétaires.

## D.3 Linux et Linus Torvalds

Vers la fin des années 1980, le projet GNU avait créé un [système d'exploitation Unix libre presque complet](http://directory.fsf.org/GNU/), mais le noyau causait des problèmes.

En 1991, indépendamment du projet GNU, Linus Torvalds, alors étudiant finlandais de 22 ans, a décidé d'écrire un noyau Unix qu'il pourrait utiliser à la maison. Plus tard dans l'année, il annonça la première sortie sur un groupe de discussion, utilisant ces mots désormais immortels : *"...I'm doing a (free) operating system (just a hobby, won't be big and professional like gnu)..."* (Je suis en train de faire un système d'exploitation (libre) (seulement un hobby, ne sera pas grand et professionnel comme gnu).

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
		<td style="width: 50%;"><div style="text-align: center;"><img style="width: 200px; height: 207px;" alt="linus" src="{{ site.baseurl | append: '/images/pics/linus.jpg' | replace: '//', '/' }}" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">Linus Torvalds</td>
	</tr>
</tbody>
</table>

Le noyau s'appelait Linux et bientôt il a été distribué sous licence GNU GPL, et les gens ont commencé à le combiner avec les outils GNU. Un système d'exploitation entièrement fonctionnel et libre de type Unix, composé de GNU et de Linux, était une réalité !

Actuellement, Linus Torvalds vit aux Etats-Unis et continue à diriger le développement du noyau Linux - mais il n'est plus seul, aujourd'hui plus d'un millier de développeurs contribuent au code du noyau chaque année - certains d'entre eux sont des volontaires qui contribuent pendant leur temps libre, tandis que d'autres sont employés par de grandes entreprises, telles que IBM, Intel, Novell et Red Hat.

## D.4 Open Source

Le terme [open source](http://opensource.org/) a été créé en 1998, par un groupe de personnes qui voulaient se distancier quelque peu de la rhétorique idéologique du mouvement du logiciel libre dans le but de rendre le logiciel libre plus attrayant aux intérêts commerciaux.

Les licences de logiciels reconnues par la Free Software Foundation et l'Open Source Initiative sont presque toutes identiques, donc il y a très peu de différence entre l'open source et le logiciel libre dans la pratique - les différences sont presque exclusivement sur un plan philosophique et rhétorique. Pour combler le fossé entre les deux camps, le terme "FOSS" (Free and Open Source Software) est souvent utilisé.

## D.5 L'histoire d'openSUSE

SUSE a été fondée le 2 septembre 1992 en Allemagne sous le nom de Gesellschaft f&uuml;r Software- und Systementwicklung mbH (S.u.S.E. GmbH) : "Développement de logiciels et de systèmes, Inc.". La première distribution GNU/Linux (S.u.S.E. Linux 1.0) est sortie en 1994, faisant de SUSE l'une des plus anciennes distributions GNU/Linux existantes. A l'origine, il s'agissait simplement d'une version allemande d'une distribution américaine appelée Slackware, mais plus tard, SUSE est devenu l'une des principales distributions. En 2003, SUSE a été racheté par Novell.

En 2005, le projet openSUSE a été lancé dans le but d'ouvrir le développement et d'impliquer davantage la communauté.

En 2010, Novell a été racheté par Attachmate. L'accord a été finalisé en avril 2011, et l'une des premières actions d'Attachmate a été de scinder SUSE en une autre entité indépendante de Novell et de transférer son siège à Nuremberg, en Allemagne. En 2014, Micro Focus a fusionné avec Attachmate, mais cela n'a pas affecté SUSE ni le projet openSUSE.

En 2014, la branche de développement openSUSE Factory a été suffisamment stabilisée pour devenir une distribution openSUSE Tumbleweed. openSUSE Tumbleweed constitue la base de SUSE Linux Enterprise Server and Desktop (SLES et SLED). Cela a de nouveau conduit à des changements dans les versions stables d'openSUSE et à la création d'openSUSE Leap en 2015, qui utilise SUSE Linux Enterprise pour le coeur du système, et a une forme de support à long terme avec de grands services packs annuels et des versions majeures ne se produisant que tous les 3-4 ans.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
<tbody>
	<tr>
		<td style="width: 25%;"><div style="text-align: center;"><img style="border: 0px solid ; width: 148px; height: 140px;" alt="gnu" src="{{ site.baseurl | append: '/images/pics/gnu-head.jpg' | replace: '//', '/' }}" /></div></td>

		<td style="width: 25%;"><div style="text-align: center;"><img style="width: 128px; height: 128px;" alt="tux" src="{{ site.baseurl | append: '/images/pics/linux.png' | replace: '//', '/' }}" /></div></td>

		<td style="width: 25%"><div style="text-align: center;"><img style="width: 120px; height: 141px;" alt="konqui" src="{{ site.baseurl | append: '/images/pics/konqui.png' | replace: '//', '/' }}" /></div></td>

		<td style="width: 25%"><div style="text-align: center;"><img style="width: 150px; height: 150px;" alt="geeko" src="{{ site.baseurl | append: '/images/pics/opensuse.jpg' | replace: '//', '/' }}" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">La mascotte du projet GNU</td>
		<td class="image-caption">La mascotte officielle de Linux - le pingouin Tux</td>
		<td class="image-caption">La mascotte de KDE - le dragon Konqui</td>
		<td class="image-caption">La mascotte de SUSE - le caméléon nommé Geeko</td>
	</tr>
</tbody>
</table>

## D.6 L'écosystème GNU/Linux

### D.6.1 Distributions

Quand le noyau Linux et les outils GNU et d'autres composants de logiciels libres "en amont" sont regroupés pour former un système d'exploitation contemporain complet, cela s'appelle une *distribution* GNU/Linux. Il existe de nombreuses distributions ciblant différents types d'utilisateurs et de cas d'utilisation - entreprises, particuliers, serveurs, ordinateurs de bureau, centres multimédia, etc. Certaines sont commerciales, d'autres reposent entièrement sur les efforts de bénévoles de la communauté. En plus d'empaqueter le logiciel, les distributeurs généralement l'intègrent, le personnalisent, le modifient, le mettent à jour, fournissent des outils supplémentaires développés en interne, etc. L'existence de distributions multiples n'est possible que parce que les composants logiciels sont bien sûr des logiciels libres.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
		<td style="width: 50%;"><center><a href="{{ site.baseurl | append: '/images/pics/ecosystem.png' | replace: '//', '/' }}" rel="thumbnail"><img src="{{ site.baseurl | append: '/images/pics/ecosystemb.png' | replace: '//', '/' }}" alt="ecosystem" class="pic" /></a></center>
    </td>			
	</tr>
  <tr>
	  <td class="image-caption">Cette figure montre l'écosystème des projets en amont, des distributeurs et des utilisateurs finaux.</td>
	</tr>
</tbody>
</table>

### D.6.2 Qui développe des logiciels libres et pourquoi ?

De nombreux développeurs sont employés par de grandes entreprises telles que IBM, Novell, Red Hat, Google, Mozilla Foundation, KDAB, Intel, AMD, Canonical, Oracle etc.  Ces entreprises ont généralement un modèle commercial de vente de services autour de logiciels libres ou de vente de matériel avec des logiciels libres installés dessus. En utilisant des logiciels libres, les entreprises peuvent partager les coûts de développement avec d'autres.

De plus, de nombreuses personnes sont payées pour développer des logiciels libres par d'autres moyens, via le travail universitaire, les parrainages gouvernementaux, les dons, les étudiants peuvent être payés via le projet[Google Summer of Code] (http://code.google.com/soc), etc.

Cependant, il y a aussi beaucoup, beaucoup de gens qui travaillent sur des logiciels libres pendant leur temps libre pour rien. Ils peuvent avoir de nombreuses motivations différentes.

- Ils peuvent avoir besoin d'une fonctionnalité ou souffrir d'un bug ("grattez là où ça vous démange").
- Il renforce leurs compétences et leur réseau et crée des opportunités d'emploi.
- La programmation est amusante et stimulante.
- Il y a beaucoup de reconnaissance et de respect à gagner.
- Vous pouvez travailler sur des projets de votre choix, contrairement à votre travail quotidien.
- Ils peuvent penser que la liberté du logiciel en soi est assez importante pour travailler.
- Ils prendront part à une communauté mondiale passionnante.
- Etc.

### D.6.3 Qui utilise GNU/Linux ?

Beaucoup de gens perçoivent encore GNU/Linux comme un petit système d'exploitation amateur - et la part de marché sur les PC de bureau standard est bien sûr assez faible. Néanmoins, une part de marché d'environ un pour cent représente encore des millions et des millions de personnes dans le monde. Aucune mesure vraiment fiable de la part de marché ou du nombre total d'utilisateurs n'est possible, pour quelque chose qui est généralement librement redistribuable.

Cependant, GNU/Linux est très répandu dans d'autres domaines. Une très grande partie des serveurs web et autres serveurs utilisent GNU/Linux. Facebook, Google et Yahoo construisent toutes leurs infrastructures sur GNU/Linux. GNU/Linux a été utilisé partout, de l'Antarctique à la NASA en passant par l'espace. GNU/Linux est le système d'exploitation préféré pour la plupart des [super ordinateurs](http://www.top500.org/stats). Et GNU/Linux est utilisé [intégré dans des périphériques](http://linuxdevices.com/) où les gens ne savent souvent même pas qu'il est là, comme les téléphones mobiles, téléviseurs, lecteurs de livres électroniques, PDA, routeurs, enregistreurs de disque dur, périphériques NAS, et plus.
