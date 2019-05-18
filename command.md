---
layout: default
title: 8. Terminal - Exécution des commandes et utilisation de l'interface de ligne de commande sur openSUSE
permalink: command
---

# 8. Terminal

Presque toutes les tâches peuvent être effectuées graphiquement sur une distribution GNU/Linux moderne comme openSUSE, mais pour vraiment devenir un utilisateur autonome et profiter pleinement de la puissance de votre système d'exploitation GNU/Linux, vous devriez au moins connaître quelques bases du terminal - ce n'est pas difficile du tout !

Il existe des milliers de commandes que vous pouvez exécuter, chacune avec un certain nombre d'options différentes. Ce chapitre n'est donc qu'un petit avant-goût décrivant les commandes les plus courantes.

Vous trouverez *Konsole* sous Système dans le menu de lancement.

{% include video.html video="konsole" screenshot="konsole" size="4.3 MB" %}

L'utilisation de la ligne de commande est assez simple. Entrez simplement une commande et éventuellement une ou plusieurs options et un ou plusieurs arguments, puis appuyez sur Entrée. Exemple :

<div class="cl">ls -l /home/[username]/ </div>

La *commande* **ls** affiche une liste de fichiers, l'*option* **-l** signifie que la liste sera affichée dans un format de liste longue, et l'*argument* **/home/[username]/** spécifie le répertoire dont le contenu est listé.

## 8.1 Raccourcis utiles

### touche tabulation

La touche de tabulation est incroyablement utile, si possible elle complétera automatiquement les commandes et arguments, ce qui vous aide à travailler plus vite et à éviter les fautes de frappe.

### Ctrl+Maj+V

Coller à partir du presse-papiers.

### Ctrl+C

Ce raccourci arrête toute opération que vous avez démarrée.

## 8.2 Exemples de commandes de base

Ceci n'est qu'une toute petite sélection de commandes pour vous donner une idée de la façon dont les choses fonctionnent.  
Le terme user dans les commandes est à remplacer par votre nom d'utilisateur.

{% include tip.html tip="Les commandes écrites en **rouge** doivent être exécutées en tant que root." %}

### 8.2.1 Gestion des fichiers et répertoires

Changer de répertoire

<div class="cl">cd /home/user/nomrepertoire/</div>

Lister les fichiers d'un répertoire

<div class="cl">ls</div>

Copier un fichier

<div class="cl">cp nomfichier /home/user/nomrepertoire/nomfichier</div>

Supprimer un fichier

<div class="cl">rm nomfichier</div>

Supprimer un répertoire et tout son contenu

<div class="cl">rm -rf /home/user/nomrepertoire</div>

Déplacer ou renommer un fichier

<div class="cl">mv /home/user/nomfichier /home/user/nouveaunomfichier</div>

### 8.2.2 Surveillance du système

Exécution des processus et consommation des ressources du système. Appuyez sur **'Q'** pour quitter.

<div class="cl">top </div>

Utilisation de l'espace disque

<div class="cl">df</div>

Consommation de mémoire

<div class="cl">free</div>

### 8.2.3 Réseau

Trouvez votre adresse IP

<div class="cl">ip a</div>

Trouvez votre passerelle (gateway)

<div class="cl">ip route</div>

Découvrez vos serveurs DNS

<div class="cl">cat /etc/resolv.conf</div>

### 8.2.4 Pages Man et aide

Presque toutes les commandes sont accompagnées d'une page de manuel décrivant comment utiliser la commande et les options disponibles. Par exemple, tapez :

<div class="cl">man cp</div>

Pour quitter à tout moment la page de manuel, appuyez sur **'Q'**.

Si une commande n'a pas de page de manuel, essayez plutôt *--help*, par exemple :

<div class="cl">cp --help</div>

### 8.2.5 Devenir Root

Pour passer à l'utilisateur root pour exécuter les tâches d'administration du système, tapez :

<div class="cl">su -</div>

Tapez ensuite votre mot de passe (root). Rien n'apparaîtra à l'écran lorsque vous tapez, ceci est voulu.

Pour arrêter de travailler en tant que root et revenir au travail en tant qu'utilisateur normal, exécutez <i>exit</i>.

<div class="clroot">exit</div>

Pour exécuter une seule commande en tant que root, utilisez :

<div class="cl">su -c "[command]"</div><p></p>

{% include note.html note="Ne travaillez pas en tant que root à moins que ce ne soit nécessaire." %}

### 8.2.6 Tâches système

Éteindre l'ordinateur :

<div class="clroot">systemctl shutdown</div>

Redémarrer :

<div class="clroot">systemctl reboot</div>

Démarrer, arrêter, redémarrer ou obtenir l'état des services système (start|stop|restart|status). Exemples:

<div class="clroot">systemctl restart network</div>
<div class="clroot">systemctl stop firewalld</div>
<div class="clroot">systemctl start apache2</div>
<div class="clroot">systemctl status smb</div>

Activez ou désactivez un service à chaque démarrage. Exemples :

<div class="clroot">systemctl enable sshd</div>
<div class="clroot">systemctl disable cups</div>

### 8.2.7 Le noyau

Découvrez la version et la nature de votre noyau :

<div class="cl">uname -r</div>

Vérifier les messages du noyau (utile pour dépanner les problèmes matériels) :

<div class="clroot">dmesg</div>

Lister les modules du noyau chargés :

<div class="clroot">lsmod</div>

Chargement d'un module du noyau :

<div class="clroot">modprobe [nommodule]</div>

Déchargement d'un module du noyau :

<div class="clroot">rmmod [nommodule]</div>

### 8.2.8 Informations sur le matériel

La commande hwinfo peut vous fournir des informations sur presque tout matériel, quelques exemples :

<div class="clroot">hwinfo --short --wlan</div>
<div class="clroot">hwinfo --short --gfxcard</div>

Lister les périphériques PCI :

<div class="clroot">lspci</div>

Lister les périphériques USB :

<div class="cl">lsusb</div>

## 8.3 Édition des fichiers texte

L'édition de fichiers de configuration ou d'autres fichiers texte peut se faire de la même manière avec l'éditeur vim, qui est installé par défaut.

Ouvrez un fichier avec *vim /path/to/file*. Exemple :

<div class="clroot">vim /etc/sysconfig/yast2</div><p></p>

{% include note.html note="Les permissions root sont utilisées dans cet exemple parce que *yast2* est un fichier de configuration système - ce n'est généralement pas nécessaire pour éditer des fichiers avec vim." %}

Appuyez sur **i** pour entrer en mode insertion (vous verrez "-- -- INSERT --" en bas de l'écran). Vous pouvez maintenant éditer le texte dans le fichier. Lorsque vous avez terminé l'édition, appuyez sur **Esc** pour quitter le mode insertion et revenir au mode commande. Tapez maintenant **:x** qui est la commande pour quitter et sauvegarder. Pour quitter sans sauvegarder les modifications, utilisez **:q!**.

Vim est assez avancé, vous pouvez envisager d'installer un éditeur de texte plus simple, par exemple essayez *nano*.

## 8.4 Lectures complémentaires

Si vous voulez en savoir plus sur l'utilisation du terminal, il existe de nombreuses ressources disponibles sur Internet, voici quelques liens.

[http://linuxcommand.org/](http://linuxcommand.org/)

[http://tldp.org/LDP/GNU-Linux-Tools-Summary/html/index.html](http://tldp.org/LDP/GNU-Linux-Tools-Summary/html/index.html)
