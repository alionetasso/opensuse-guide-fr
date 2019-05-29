---
layout: default
title: 10. Paramètres administrateur (YaST) - Introduction à l'outil de configuration YaST
permalink: yast
---

# 10. Paramètres administrateur (YaST)

YaST (*Y*et *a*nother *S*etup *T*ool : encore un autre outil de configuration) est l'outil central de l'administration du système. Vous pourrez trouver YaST dans le menu principal, dans la catégorie Système (ou en faisant une recherche dans le shell si vous utilisez GNOME).

{% include screenshot.html image="yast-controlcenter" %}

**Modules YaST par défaut**

Depuis YaST, vous pouvez effectuer à peu près n'importe quelle tâche d'administration du système à l'aide de modules graphiques puissants. Par exemple :

- Installer et supprimer des logiciels (voir chapitre suivant)
- Configurer votre imprimante
- Configurer votre pare-feu
- Activer ou désactiver les services du système
- Paramétrer vos partages de fichiers (samba)
- Gérer le partionnement de vos disques
- Activer le daemon NTP
- Et bien plus encore...


**Modules YaST complémentaires**

En plus de ceux présents dans l'installation par défaut, de nombreux autres modules YaST sont disponibles (découvrez comment installer de nouveaux paquets au chapitre suivant). Quelques uns de ces modules les plus importants sont :

- Gestion du serveur Web Apache (package: yast2-http-server)
- Configuration du daemon SSH (package: yast2-sshd)
- Serveur FTP (package: yast2-ftp-server)
- Serveur NFS (package: yast2-nfs-server)
- Et il en existe encore d'autres...

{% include tip.html tip="Vous n'êtes pas tenus d'utiliser YaST si vous ne le souhaitez pas. Vous pouvez effectuer les mêmes tâches grâce à des outils en ligne de commande et en éditant manuellement les fichiers de configuration." %}

## 10.1 YaST en terminal

Les modules YaST peuvent aussi être utilisés depuis un terminal (en mode ncurses), ce qui est particulièrement utile sur des serveurs ne disposant pas d'environnement graphique, dans le cadre d'un accès via SSH ou encore si votre environment graphique rencontrait un problème.

Pour cela, exécutez simplement la commande *yast* en tant que root dans un terminal.

<div class="clroot">yast</div><p></p>

{% include screenshot.html image="yast-ncurses" %}

Naviguez en utilisant les touches fléchées, Entrée et Alt+[lettres en surbrillance](ex. Alt+Q pour quitter).
