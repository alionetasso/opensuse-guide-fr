---
layout: default
title: 14. Codecs Multimedia - Installez la prise en charge des codecs avec restrictions comme MP3, DVD, WMA, WMV, MOV, etc.
permalink: codecs
---

# 14. Codecs multimédia

Ce chapitre décrit deux méthodes différentes pour installer les paquets nécessaires à la lecture de la plupart des formats multimédias, y compris MP3, DVD, etc., avec le lecteur multimédia par défaut VLC. Vous pouvez utiliser l'installation manuelle en 1 clic ou utiliser la ligne de commande - selon la méthode que vous préférez.

Par défaut, seuls les formats libres, ouverts et non protégés par un brevet tels que Ogg Theora, Ogg Vorbis et Flac sont supportés pour des raisons légales (brevets logiciels américains et Digital Millennium Copyright Act (DMCA)).


## 14.1 Installation des codecs en 1-Click

1) Cliquez sur le bouton ci-dessous pour ajouter les dépôts nécessaires et installer les paquets requis en 1 clic.

{% include ymp.html icon="codecs" link="http://opensuse-community.org/codecs-kde.ymp" %}

{% include tip.html tip="Si une boîte de dialogue de conflit apparaît, sélectionnez pour installer les paquets *avec* Changement de fournisseur." %}

2) Ensuite, assurez-vous que tous vos paquets multimédia proviennent du dépôt Packman :

<div class="path">Démarrer YaST => Installez et supprimez des logiciels => Cliquez sur Vue => Cliquez sur Dépôts => Sélectionnez le dépôt Packman => Cliquez "Remplacez les paquets système par les versions de ce dépôt (Packman Repository)" => Cliquez sur "Accepter"</div><p></p>

{% include screenshot.html image="packman-vendorchange" %}

## 14.2 Installation des codecs dans le terminal

Pour installer les codecs à l'aide du terminal, procédez comme suit :

{% include tip.html tip="Utilisez la fonction Copier/Coller pour éviter les fautes de frappe. Pour coller dans Konsole, cliquez avec le bouton droit de la souris => Coller - ou utilisez **Ctrl+Maj+V**." %}

1) Ajoutez les dépôts nécessaires :

<div class="clroot">zypper addrepo -f 'https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Leap_$releasever/' packman</div>
<div class="clroot">zypper addrepo -f http://opensuse-guide.org/repo/openSUSE_Leap_15.2/ dvd</div>

2) Ensuite, installez les paquets nécessaires :

<div class="clroot">zypper install --allow-vendor-change ffmpeg-3 lame gstreamer-plugins-bad gstreamer-plugins-ugly gstreamer-plugins-ugly-orig-addon gstreamer-plugins-libav libavdevice58 libdvdcss2 vlc-codecs</div>

3) Assurez-vous que tous vos paquets multimédia proviennent du dépôt Packman :

<div class="clroot">zypper dup --allow-vendor-change --from packman/</div>
