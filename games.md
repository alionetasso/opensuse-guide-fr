---
layout: default
title: "Annexe B: Jeux - Jouer à des jeux sur openSUSE"
permalink: jeux
---

# Annexe B: Jeux

Tous les grands jeux grand public ne fonctionnent pas nativement sous GNU/Linux, mais il y a encore beaucoup de possibilités de jeu.

<center><img src="{{ site.baseurl | append: '/images/pics/spil.jpg' | replace: '//', '/' }}" alt="spil" class="pic" /></center>

## B.1 Jeux GNU/Linux natifs

### B.1.1 Dépôt pour les jeux : openSUSE Build Service Games Repository

Certains jeux sont inclus dans les dépôts officiels d'openSUSE, mais le dépôt Games sur openSUSE Build Service contient beaucoup plus de jeux. Vous pouvez facilement ajouter ce dépôt via la liste des dépôts communautaires comme décrit dans le chapitre [Dépôts de logiciels](depots).

Ou ajoutez le référentiel de jeux en utilisant la ligne de commande :

<div class="clroot">zypper addrepo -f http://download.opensuse.org/repositories/games/openSUSE_Leap_15.3/ games</div>

### B.1.2 Plate-forme et magasin de jeux Steam Gaming

La [Plate-forme de jeu et magasin Steam](http://store.steampowered.com/browse/linux/) est disponible pour GNU/Linux. Vous pouvez en trouver des paquets [ici](http://software.opensuse.org/package/steam).

### B.1.3 itch.io/games

itch.io est un marché ouvert pour les créateurs numériques indépendants qui se concentre sur les jeux vidéo indépendants. C'est une plateforme qui permet à chacun de vendre le contenu qu'il a créé. itch.io est aussi une collection de certaines des créations les plus uniques, intéressantes et indépendantes que vous trouverez sur le web. Voir :

[https://itch.io/games/platform-linux](https://itch.io/games/platform-linux)

### B.1.4 Autres ressources de jeux pour GNU/Linux

Linux Game Publishing achète des titres et les porte vers GNU/Linux, voir :

[http://www.linuxgamepublishing.com](http://www.linuxgamepublishing.com) (n'existe plus depuis 2014)

Il existe de plus en plus de jeux gratuits et/ou non-libres - certains petits et simples, d'autres assez grands, et beaucoup de très bons. Consultez certains de ces sites :

[http://www.penguspy.com/](http://www.penguspy.com/)

[https://www.gog.com/games](https://www.gog.com/games)

[https://www.humblebundle.com/store](https://www.humblebundle.com/store)

Enfin une recherche sur le web vous permettra de trouver d'autres liens comme par exemple cette chaînes youtube francophone :

[Gaming Linux FR](https://www.youtube.com/user/vinceff44/featured)

## B.2 Exécution des jeux MS Windows

Certains logiciels disponibles pour GNU/Linux vous permettent d'exécuter des jeux développés pour MS Windows sous GNU/Linux - la facilité d'utilisation et le taux de réussite peuvent varier - cependant, plus le jeu est populaire, plus il a de chances d'être supporté.

### B.2.1 Wine

Wine (Wine Is Not an Emulator) est la première option, c'est un logiciel gratuit installable via le gestionnaire de paquets. Consultez la base de données de l'application Wine pour plus d'informations sur l'exécution de jeux individuels :

[http://appdb.winehq.org/appbrowse.php?iCatId=2](http://appdb.winehq.org/appbrowse.php?iCatId=2)

Wine est une application en ligne de commande, la syntaxe est :

<div class="cl">wine /path/to/setup.exe</div>

### B.2.2 PlayOnLinux

[PlayOnLinux](http://www.playonlinux.com/) est basé sur Wine et vous permet d'installer et d'utiliser facilement (certains) jeux MS Windows. Vous pouvez trouver des paquets de PlayOnLinux dans le dépôt de jeux mentionné ci-dessus.

### B.2.3 CrossOver Games

CrossOver est un programme commercial et propriétaire basé sur Wine. Voir :

[https://www.codeweavers.com/products/cxgames/](https://www.codeweavers.com/products/cxgames/)

### B.2.4 Lutris

[Lutris](https://lutris.net/) permet de rassembler et de gérer (installer, configurer et lancer) tous les jeux acquis depuis n'importe quelle source, dans une interface unique. Cela inclut, par exemple, les jeux Steam, GOG, Battle.net, Origin, Uplay, les jeux Windows (WINE), ou les jeux sur console émulés et les jeux par navigateur.

## B.3 Émulateurs

De nombreux émulateurs existent, permettant d'exécuter de nombreux anciens jeux classiques d'autres plates-formes sur GNU/Linux. Par exemple :

- Amiga (UAE)
- Arcade (MAME)
- Atari (Stella, Steem)
- Commodore 64/128 (VICE)
- MS DOS (DOSBox, DOSEMU)
- Nintendo (infones, bsnes, nestopia)
- Play Station (pcsx, pcsx2)

{% include tip.html tip="Habituellement, vous ne pouvez le faire légalement que si vous possédez le DVD/une licence pour celui-ci." %}
