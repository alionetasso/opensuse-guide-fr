---
layout: default
title: "Appendix C: Under the Hood - A Look at What's Happening Under the Surface"
title: "Annexe C: Dans les coulisses - À la découverte de ce qu'il se passe sous la surface"
permalink: under
---

# Appendix C: Sous la surface

The purpose of this chapter is to give the reader a quick look and basic idea of what's going on beneath the surface of the openSUSE GNU/Linux operating system.
L'objectif de ce chapitre est de donner au lecteur un aperçu et quelques idées de ce qu'il se passe dans les rouages d'un système d'exploitation openSUSE GNU/Linux.

## C.1 Composants principaux du système

Any modern computer operating system is a very large and complicated contraption - and GNU/Linux distributions are no exception. The Linux kernel is just one of many components. The figure below shows the core components and what their respective roles are.
N'importe quel système d'exploitation moderne est un immense et complexe engin, et les distributions GNU/Linux ne font pas exception. Le noyau Linux n'est qu'un composant parmi bien d'autres. L'illustration ci-dessous présente les composants essentiels et leur rôle.

<table style="text-align: left; width: 100%;" border="0" cellpadding="2" cellspacing="2">
        <tbody>
        <tr>
        <td style="width: 50%;"><center><a href="{{ site.baseurl | append: '/images/pics/distro.png' | replace: '//', '/' }}" rel="thumbnail"><img src="{{ site.baseurl | append: '/images/pics/distrob.png' | replace: '//', '/' }}" alt="distro" class="pic" /></a></center><br /></td>
        </tr>
        <tr>
        <td class="image-caption">Cette illustration présente les principaux composants d'un système GNU/Linux</td>
        </tr>
        </tbody>
</table>

## C.2 Aborescence

Most users will hardly ever need to work outside their home folder, but nevertheless it's probably a good idea to have a basic idea about the how the file hierarchy works.
La plupart des utilisateurs n'auront probablement jamais besoin de travailler en dehors de leur dossier *home*. Il n'est toutefois par inutile d'avoir une petite idée du fonctionnement de la hiérarchie des fichiers.

On GNU/Linux you only have *one* file tree, unlike e.g. Microsoft Windows which has a different file tree for each filesystem/partition - on GNU/Linux separate filesystems/partitions are *mounted* in folders within a single file tree. The root folder for the file tree is "**/**" and paths are written using forward slashes.
Chez GNU/Linux, il n'y a *qu'une seule* arborescence, contrairement à Microsoft Windows, par exemple, qui dispose d'arborescences différentes pour chacun des systèmes de fichiers et partitions, sous GNU/Linux les systèmes de fichiers ou partitions séparés sont *montés* dans des dossiers au sein d'une seule et même arborescence. Le dossier racine de l'arborescence est "**/**" et les chemins sont écrits à la suite en utilisant d'autre slashes.

So a path might look like this in GNU/Linux:
En conséquence, un chemin ressemblera à cela sous GNU/Linux :

**/home/*username*/Bureau/**

In MS Windows a comparable path might look like this:
Chez MS Windows, ce même chemin ressemblerait à cela :

**C:\\Documents and Settings\\*username*\\Desktop**

{% include tip.html tip="In GNU/Linux filenames and folders are **case sensitive**." %}
{% include tip.html tip="Sous GNU/Linux les noms de fichiers et de dossiers sont **sensibles à la casse (majuscule/minuscule)**." %}

Normal users only have write permission in their **/home/** folder, and rarely have any need to work outside of that.
Les utilisateurs normaux ne disposent de permissions en écriture qu'à l'intérieur de leur dossier **/home/** et n'ont que très rarement le besoin de travailler en dehors de ce dernier.

## C.3 Fichiers cachés

Files and folders starting with '.' (dot) are hidden. You can make them visible in Dolphin file manager via the keyboard shortcut **Alt+.** or **View -&gt; Show Hidden Files** in the menubar.
Les fichiers et dossiers dont le nom commence par '.' (un point) sont cachés. Sous Dolphin, vous pouvez les afficher via le raccourci clavier **Alt+.** ou via le menu **Affichage → Afficher les fichiers masqués** dans la barre de menu. Sous Nautilus, le gestionnaire de fichiers de GNOME, vous pouvez les afficher via le raccourci clavier **Ctrl+h** ou via le menu dit *hamburger*, en haut à droite puis en cochant **Afficher les fichiers masqués**.

Applications store the user settings and data in hidden folders in the users home folder, e.g. **/home/*username*/.mozilla/** or **/home/*username*/.config/vlc/** etc. If you uninstall/reinstall an application the settings and data will remain in the home folder. To "reset" an application, you just rename or (re)move the settings and/or data hidden in your home folder.
Les applications enregistrent les paramètres des utilisateurs et certaines données qu'elles utilisent dans le dossier *home* des utilisateurs, par exemple sous **/home/*utilisateur*/.mozilla/** ou **/home/*utilisateur*/.config/vlc/** etc. Si vous désinstallez ou réinstallez une application, ses paramètres et données resteront dans le dossier *home*. Pour réinitialiser une application, il vous suffit de renommer, déplacer ou supprimer ces paramètres et données, masqués dans votre dossier *home*.

## C.4 Important Config Files

In GNU/Linux configurations and settings are usually stored in human-readable plain text files. Almost any configuration can be done graphically via YaST or various other GUI applications, but nevertheless it can be useful to know the location of some key config files.

System wide configurations are mainly stored in **/etc/**, user settings are stored in hidden files in the home folder for the individual user.

<table class="table">
<tbody>
    <tr>
    <td style="width: 230px;"><b>/etc/fstab</b></td>
    <td>The file system table, file systems/partitions mounted during boot.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/sysconfig/yast2</b></td>
    <td>Configuration for YaST.</td>
    </tr>
    <tr>
    <td style="width: 230px;"><b>/etc/zypp/zypp.conf</b></td>
    <td>Configuration for the software management.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/samba/smb.conf</b></td>
    <td>Samba configuration ("Windows Network")</td>
    </tr>
    <tr>
    <td style="width: 230px;"><b>/etc/HOSTNAME</b></td>
    <td>The hostname for the machine.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/X11/xorg.conf.d/</b></td>
    <td>X-server configuration files. By default autodetection is used, edit these files if you must configure the X-server.</td>
    </tr>
    <tr>
    <td style="width: 230px;"><b>/etc/sysconfig/kernel</b></td>
    <td>The kernel. For example loading extra modules during boot.</td>
    </tr>
    <tr class="d1">
    <td style="width: 230px;"><b>/etc/modprobe.d/50-blacklist.conf</b></td>
    <td>Blacklisting kernel modules.</td>
    </tr>
</tbody>
</table>


## C.5 Logs

In case of problems it's good to know the location of the main log files, most are kept in **/var/log/**.

<table class="table">
<tbody>
  <tr>
      <td style="width: 230px;"><b>/var/log/Xorg.0.log</b></td>
      <td>Log for the X-server.</td>
  </tr>
  <tr class="d1">
      <td style="width: 230px;"><b>/home/<i>username</i>/.xsession-errors</b></td>
      <td>Useful for troubleshooting applications ran as normal user.</td>
  </tr>
  <tr class="d1">
      <td style="width: 230px;"><b>/var/log/YaST2/</b></td>
      <td>Log files for various YaST modules and components.</td>
  </tr>
  </tbody>
</table>

The main system log can be viewed with the YaST module *systemd-journal* or with the command journalctl:

<div class="clroot">journalctl</div>

Read up on journalctl to use it effectively.

## C.6 Troubleshooting

Here are some basic troubleshooting tips for GNU/Linux in case an application crashes or won't start at all.

- If an application fails, try running it from a terminal to get more/better output
- Try removing/renaming the hidden folder(s) for the application in the users home folder
- Try creating a new user and see if the problem persists. If the problem does not persist for a new user, the cause can probably be found in the settings/data in the home folder of the user with the problem
- Check out relevant log files

{% include tip.html tip="Reinstalling the software packages almost never solves anything, because the old settings and data will remain in hidden folders in the home folder." %}
