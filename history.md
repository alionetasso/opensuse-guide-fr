---
layout: default
title: "Appendix D: Histoire et contexte - Qu'est-ce que le Logiciel Libre et Open Source et Quelle est l'histoire d'openSUSE ?"
permalink: histoire
---

# Appendix D: Histoire et contexte

Le but de ce chapitre est de donner aux lecteurs un aperçu et une connaissance de base de l'histoire et de l'écosystème de GNU/Linux et des logiciels libres/open source en général..

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

En 1984 et 1985 respectivement, le programmeur système Richard M. Stallman (RMS), de plus en plus frustré par les restrictions techniques et sociales imposées par les logiciels propriétaires, créa le projet [GNU](http://www.gnu.org/) (GNU's Not Unix) afin de créer un système d'exploitation libre semblable à Unix et la [Free Software Foundation (FSF)] (http://www.fsf.org) une fondation visant à promouvoir les logiciels libres.

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

En 1991, indépendamment du projet GNU, Linus Torvalds, alors étudiant finlandais de 22 ans, a décidé d'écrire un noyau Unix qu'il pourrait utiliser à la maison. Plus tard dans l'année, il annonça la première sortie sur un groupe de discussion, utilisant ces mots désormais immortels : *"...I'm doing a (free) operating system (just a hobby, won't be big and professional like gnu)..."*.

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

Aujourd'hui, Linus Torvalds vit aux Etats-Unis et continue à diriger le développement du noyau Linux - mais il n'est plus seul, aujourd'hui plus d'un millier de développeurs contribuent au code du noyau chaque année - certains d'entre eux sont des volontaires qui contribuent pendant leur temps libre, tandis que d'autres sont employés par de grandes entreprises, telles que IBM, Intel, Novell et Red Hat.

## D.4 Open Source

Le terme [open source](http://opensource.org/) a été créé en 1998, par un groupe de personnes qui voulaient se distancier quelque peu de la rhétorique idéologique du mouvement du logiciel libre dans le but de rendre le logiciel libre plus attrayant aux intérêts commerciaux.

Les licences de logiciels reconnues par la Free Software Foundation et l'Open Source Initiative sont presque toutes identiques, donc il y a très peu de différence entre l'open source et le logiciel libre dans la pratique - les différences sont presque exclusivement sur un plan philosophique et rhétorique. Pour combler le fossé entre les deux camps, le terme "FOSS" (Free and Open Source Software) est souvent utilisé.

## D.5 The History of openSUSE

SUSE was founded on September 2, 1992 in Germany, under the name Gesellschaft f&uuml;r Software- und Systementwicklung mbH (S.u.S.E. GmbH), meaning: "Software and System Development, Inc.". The first GNU/Linux distribution (S.u.S.E. Linux 1.0) was released in 1994 - making SUSE one of the oldest existing GNU/Linux distributions. Originally it was merely a German version of an American distribution called Slackware, but later SUSE has become one of the leading distributions. In 2003 SUSE was acquired by Novell.

In 2005 the openSUSE project was started with the goal of opening up development and involve the community more.

In 2010 Novell was acquired by Attachmate. The deal was finalized in April 2011, and one of the first actions of Attachmate was to split SUSE into a separate business unit independant of Novell, and move SUSE headquarters back to Nuremberg, Germany. In 2014 Micro Focus merged with Attachmate, but this did not affect SUSE nor the openSUSE Project.

In 2014 the development branch openSUSE Factory was stabilized enough to become a usable rolling relese distribution, called openSUSE Tumbleweed. openSUSE Tumbleweed forms the base for SUSE Linux Enterprise Server and Desktop (SLES and SLED). This again lead to changes in the stable openSUSE releases and the creation of openSUSE Leap in 2015, which uses SUSE Linux Enterprise for the core system, and has a form of long term support with major yearly service packs and major releases only happening every 3-4 years.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
<tbody>
	<tr>
		<td style="width: 25%;"><div style="text-align: center;"><img style="border: 0px solid ; width: 148px; height: 140px;" alt="gnu" src="{{ site.baseurl | append: '/images/pics/gnu-head.jpg' | replace: '//', '/' }}" /></div></td>

		<td style="width: 25%;"><div style="text-align: center;"><img style="width: 128px; height: 128px;" alt="tux" src="{{ site.baseurl | append: '/images/pics/linux.png' | replace: '//', '/' }}" /></div></td>

		<td style="width: 25%"><div style="text-align: center;"><img style="width: 120px; height: 141px;" alt="konqui" src="{{ site.baseurl | append: '/images/pics/konqui.png' | replace: '//', '/' }}" /></div></td>

		<td style="width: 25%"><div style="text-align: center;"><img style="width: 150px; height: 150px;" alt="geeko" src="{{ site.baseurl | append: '/images/pics/opensuse.jpg' | replace: '//', '/' }}" /></div></td>
	</tr>
      	<tr>
		<td class="image-caption">The GNU project mascot</td>
		<td class="image-caption">The official mascot of Linux - the penguin Tux</td>
		<td class="image-caption">The KDE mascot - the dragon Konqui</td>
		<td class="image-caption">The SUSE mascot - the chameleon named Geeko</td>
	</tr>
</tbody>
</table>

## D.6 The GNU/Linux Ecosystem

### D.6.1 Distributions

When the Linux kernel and the GNU tools and other free software components from "upstream" are bundled together to form a complete contemporary operating system, it's called a  GNU/Linux *distribution*. Many distributions exist targetting different types of users and use cases - enterprises, home users, servers, desktops, multimedia centers etc. Some are commercial, others are fully based on the efforts of community volunteers. Besides bundling the software, distributors usually also integrate it, brand it, patch it, provide additional tools developed in-house and so forth. The existence of multiple distributions is only possible because the software components are free software of course.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
	<tbody>
	<tr>
		<td style="width: 50%;"><center><a href="{{ site.baseurl | append: '/images/pics/ecosystem.png' | replace: '//', '/' }}" rel="thumbnail"><img src="{{ site.baseurl | append: '/images/pics/ecosystemb.png' | replace: '//', '/' }}" alt="ecosystem" class="pic" /></a></center>
    </td>			
	</tr>
  <tr>
	  <td class="image-caption">This figure shows the ecosystem of upstream projects, distributors and end users.</td>
	</tr>
</tbody>
</table>

### D.6.2 Who Develops Free Software and Why?

Many developers are employed by large companies such as IBM, Novell, Red Hat, Google, Mozilla Foundation, KDAB, Intel, AMD, Canonical, Oracle etc. These companies usually have a business model of selling services around free software or selling hardware with free software installed on it. By using free software companies can share the development costs with others.

Also many people are paid to develop free software in other ways, via university work, government sponsorships, donations, students can be paid via the [Google Summer of Code](http://code.google.com/soc) project, etc.

However there are also many, many people working on free software in their spare time for nothing. They can have many different motivations.

- They may need a feature or suffer a bug ("scratch your own itch").
- It builds their skills and network and creates job opportunities.
- Programming is fun and challenging.
- There's a lot of recognition and respect to be gained.
- You can work on projects of you own choosing, unlike at your day-job.
- They may think software freedom in itself is important enough to work for.
- They'll take part in an exciting worldwide community.
- Etc.

### D.6.3 Who is Using GNU/Linux?

Many people still perceive GNU/Linux as a small hobbyist operating system - and the marketshare on standard desktop PCs is quite small of course. Nevertheless a marketshare of about one percent, still adds up to millions and millions of people worldwide. No truly reliable measure of the marketshare or total number of users is possible, for something which is usually freely redistributable.

However GNU/Linux is very widespread in other areas. A very large share of web servers and other servers run GNU/Linux. Facebook, Google and Yahoo build their entire infrastructures on GNU/Linux. GNU/Linux has been used everywhere from Antarctica to NASA using it in outer space. GNU/Linux is the preferred operating system for most of the world's [super computers](http://www.top500.org/stats). And GNU/Linux is used [embedded in devices](http://linuxdevices.com/) where people often don't even know it's there, such as mobile phones, TVs, e-book-readers, PDAs, routers, hard disk recorders, NAS devices, and more.
